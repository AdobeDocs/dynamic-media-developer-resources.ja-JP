---
description: キャッシュエントリは、CacheValidationPolicy（default.iniまたは特定の画像カタログの.iniファイル）属性で選択された、カタログベースまたは有効期限ベースのキャッシュ検証を使用して、自動的に更新されます。
seo-description: キャッシュエントリは、CacheValidationPolicy（default.iniまたは特定の画像カタログの.iniファイル）属性で選択された、カタログベースまたは有効期限ベースのキャッシュ検証を使用して、自動的に更新されます。
seo-title: 応答キャッシュの検証
solution: Experience Manager
title: 応答キャッシュの検証
topic: Scene7 Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 応答キャッシュの検証{#response-cache-validation}

キャッシュエントリは、（default.ini内の）attribute::CacheValidationPolicyまたは特定の画像カタログの.iniファイルで選択された、カタログベースまたは有効期限ベースのキャッシュ検証を使用して、自動的に更新されます。

カタログベースの検証では、既存のキャッシュエントリがキャッシュエントリの作成時刻よりも新しい場合(またはフ `catalog::LastModified` ァイルのファイル変更時刻 `attribute::LastModified`[!DNL catalog.ini] )、既存のキャッシュエントリが古いと見なされます。

有効期限ベースの検証では、最新の検証から5分後にキャッシュエントリが古くなります。 どちらの場合も、サーバーは、要求の作成に関与したすべての画像ファイルのファイル日付を確認することで、古いキャッシュエントリを検証します。 ファイルの日付が変更されていない場合は、キャッシュエントリのタイムスタンプが更新され、キャッシュされた日付が有効と見なされます。

画像カタログに登録された画像がほとんど含まれる一般的なアプリケーションでは、カタログベースの検証を使用するとパフォーマンスが向上します。 画像カタログを使用しないアプリケーションでは、有効期限ベースのキャッシュ検証を使用する必要があります。 これを行う方法の1つは、でを設定し、 `attribute::cacheValidationPolicy=0` すべての [!DNL default.ini]特定の画像カタ `1` ログファイルにを設定することです。

キャッシュエントリは無効になり、要求に関わるカタログエントリが、返信画像の変更の原因となるように変更された場合に、再生成される可能性があります。 例えば、変更の内容など `catalog::Modifier` です。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Scene7ピラミッドTIFF(PTIFF)画像は、検証のためにファイルヘッダー内のファイル日付を内部で保持します。 ファイルシステムで保持されるファイル変更時間は、非PTIFFファイルが変更されたかどうかを確認するために使用されます。

キャッシュの検証プロセスには、画像ファイルのみが関与します。 フォントファイルまたはICCプロファイルファイルを変更しても、キャッシュエントリは自動的に無効になりません。

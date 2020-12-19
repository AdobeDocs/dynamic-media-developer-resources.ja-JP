---
description: キャッシュエントリは、CacheValidationPolicy属性（default.ini内または特定の画像カタログの.iniファイル内）で選択された、カタログベースまたは有効期限ベースのキャッシュ検証を使用して自動的に更新されます。
seo-description: キャッシュエントリは、CacheValidationPolicy属性（default.ini内または特定の画像カタログの.iniファイル内）で選択された、カタログベースまたは有効期限ベースのキャッシュ検証を使用して自動的に更新されます。
seo-title: 応答キャッシュの検証
solution: Experience Manager
title: 応答キャッシュの検証
topic: Scene7 Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# 応答キャッシュの検証{#response-cache-validation}

キャッシュエントリは、attribute::CacheValidationPolicy（default.ini内、または特定の画像カタログの.iniファイル内）で選択された、カタログベースまたは有効期限ベースのキャッシュ検証を使用して自動的に更新されます。

カタログベースの検証では、`catalog::LastModified`（または`attribute::LastModified`）（または[!DNL catalog.ini]ファイルのファイル変更時刻）がキャッシュエントリの作成時刻より新しい場合、既存のキャッシュエントリは古いと見なされます。

有効期限ベースの検証では、最新の検証から5分後にキャッシュエントリが古くなります。 どちらの場合も、サーバーは、要求の作成に関係したすべての画像ファイルのファイル日付をチェックして、古いキャッシュエントリを検証します。 ファイルの日付が変更されていない場合は、キャッシュエントリのタイムスタンプが更新され、キャッシュされた日付が有効と見なされます。

ほとんどの画像が画像カタログに登録されている一般的なアプリケーションでは、カタログベースの検証によってパフォーマンスが向上します。 画像カタログを使用しないアプリケーションでは、有効期限ベースのキャッシュ検証を使用する必要があります。 これを行う1つの方法は、[!DNL default.ini]の`attribute::cacheValidationPolicy=0`を、すべての特定の画像カタログファイルの`1`に設定することです。

キャッシュエントリは無効になり、要求に関連するカタログエントリが、返信画像に変更が生じる可能性のある方法で変更された場合に、再生成されます。 例えば、`catalog::Modifier`の内容が変わります。

>[!NOTE]
>
>Scene7ピラミッドTIFF(PTIFF)画像は、検証のためにファイルヘッダー内にファイルの日付を内部的に保持します。 ファイルシステムによって保持されるファイル変更時間は、非PTIFFファイルが変更されたかどうかを確認するために使用されます。

キャッシュの検証プロセスに関与するのは画像ファイルのみです。 フォントファイルやICCプロファイルファイルを変更しても、キャッシュエントリは自動的に無効になりません。

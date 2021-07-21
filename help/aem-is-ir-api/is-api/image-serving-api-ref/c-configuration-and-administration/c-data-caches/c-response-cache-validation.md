---
description: キャッシュエントリは、CacheValidationPolicy属性（default.ini内または特定の画像カタログの.iniファイル）で選択されたように、カタログベースまたは有効期限ベースのキャッシュ検証を使用して自動的に更新されます。
solution: Experience Manager
title: 応答キャッシュの検証
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 応答キャッシュの検証{#response-cache-validation}

キャッシュエントリは、attribute::CacheValidationPolicy（default.ini内または特定の画像カタログの.iniファイル内）で選択されたように、カタログベースまたは有効期限ベースのキャッシュ検証を使用して自動的に更新されます。

カタログベースの検証では、`catalog::LastModified`（または`attribute::LastModified`、または[!DNL catalog.ini]ファイルのファイル変更時刻）がキャッシュエントリが作成された時刻より新しい場合、既存のキャッシュエントリが古いと見なされます。

有効期限ベースの検証では、最新の検証以降、5分後にキャッシュエントリが古くなります。 どちらの場合も、サーバーは、リクエストの作成に関係したすべての画像ファイルのファイル日付を確認することで、古いキャッシュエントリを検証します。 ファイルの日付が変更されていない場合、キャッシュエントリのタイムスタンプが更新され、キャッシュされた日付が有効と見なされます。

ほとんどの画像が画像カタログに登録されている一般的なアプリケーションでは、カタログベースの検証がパフォーマンスを向上させます。 画像カタログを含まないアプリケーションでは、有効期限ベースのキャッシュ検証を使用する必要があります。 これを実現する1つの方法は、 [!DNL default.ini]で`attribute::cacheValidationPolicy=0`を設定し、すべての特定の画像カタログファイルで`1`を設定することです。

リクエストに含まれるカタログエントリが応答画像の変更を引き起こす可能性のある方法で変更されると、キャッシュエントリが無効になり、再生成される可能性があります。 例えば、`catalog::Modifier`の内容が変わります。

>[!NOTE]
>
>Dynamic Media PTIFF(Pyramid TIFF)画像は、検証目的で、ファイルヘッダー内のファイルの日付を内部的に保持します。 ファイルシステムによって保持されるファイル変更時刻は、非PTIFFファイルが変更されたかどうかを確認するために使用されます。

キャッシュ検証プロセスには画像ファイルのみが含まれます。 フォントファイルまたはICCプロファイルファイルに対する変更は、キャッシュエントリの自動無効化の原因になりません。

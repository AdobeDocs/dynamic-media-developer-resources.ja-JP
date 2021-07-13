---
description: 画像サービングは、外部のHTTPおよびFTPサーバー上のソース画像へのアクセスをサポートします。
solution: Experience Manager
title: 外部画像ソース
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 外部画像ソース{#foreign-image-sources}

画像サービングは、外部のHTTPおよびFTPサーバー上のソース画像へのアクセスをサポートします。

`src=`または`mask=`コマンドの外部URLを指定するには、次のようにします。埋め込みURL全体を中括弧で区切るだけです。

` …&src={ *[!DNL foreignUrl]*}&…`

完全な絶対URL（`attribute::AllowDirectUrls`が設定されている場合）と`attribute::RootUrl`に対する相対URLが許可されます。 絶対URLが埋め込まれ、次の属性がある場合、エラーが発生します。`AllowDirectUrls`は0か、相対URLが指定され、`attribute::RootUrl`が空の場合。

外部画像は、HTTP応答に含まれるキャッシュヘッダーに従って、サーバーによってキャッシュされます。

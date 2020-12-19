---
description: 画像サービングでは、外部のHTTPサーバおよびFTPサーバ上のソース画像へのアクセスがサポートされています。
seo-description: 画像サービングでは、外部のHTTPサーバおよびFTPサーバ上のソース画像へのアクセスがサポートされています。
seo-title: 外部画像ソース
solution: Experience Manager
title: 外部画像ソース
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# 外部画像ソース{#foreign-image-sources}

画像サービングでは、外部のHTTPサーバおよびFTPサーバ上のソース画像へのアクセスがサポートされています。

`src=`または`mask=`コマンドの外部URLを指定するには；埋め込まれたURL全体を波括弧で囲みます。

` …&src={ *[!DNL foreignUrl]*}&…`

完全な絶対URL（`attribute::AllowDirectUrls`が設定されている場合）および`attribute::RootUrl`を基準としたURLを使用できます。 絶対URLが埋め込まれ、属性が次の場合にエラーが発生します。`AllowDirectUrls`が0の場合、または相対URLが指定され、`attribute::RootUrl`が空の場合。

外部イメージは、HTTP応答に含まれるキャッシュヘッダーに従ってサーバーによってキャッシュされます。

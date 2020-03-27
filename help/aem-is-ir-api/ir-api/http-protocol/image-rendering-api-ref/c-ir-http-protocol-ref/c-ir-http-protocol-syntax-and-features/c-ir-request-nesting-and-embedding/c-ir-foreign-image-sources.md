---
description: 画像サービングは、外部のHTTPおよびFTPサーバ上のソース画像へのアクセスをサポートします。
seo-description: 画像サービングは、外部のHTTPおよびFTPサーバ上のソース画像へのアクセスをサポートします。
seo-title: 外部画像ソース
solution: Experience Manager
title: 外部画像ソース
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 外部画像ソース{#foreign-image-sources}

画像サービングは、外部のHTTPおよびFTPサーバ上のソース画像へのアクセスをサポートします。

またはコマンドの外部URLを指 `src=` 定するに `mask=` は：埋め込まれたURL全体を波括弧で囲みます。

` …&src={ *[!DNL foreignUrl]*}&…`

完全な絶対URL(設定さ `attribute::AllowDirectUrls` れている場合)と相対URLが許可 `attribute::RootUrl` されます。 絶対URLが埋め込まれ、属性が次の場合にエラーが発生します。が0 `AllowDirectUrls` の場合、または相対URLが指定されていて空の場 `attribute::RootUrl` 合。

外部画像は、HTTP応答に含まれるキャッシュヘッダーに従って、サーバーによってキャッシュされます。

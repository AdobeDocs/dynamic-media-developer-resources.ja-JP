---
title: 外部画像ソース
description: 画像サービングは、外部 HTTP サーバーおよび FTP サーバー上のソース画像へのアクセスをサポートします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# 外部画像ソース{#foreign-image-sources}

画像サービングは、外部 HTTP サーバーおよび FTP サーバー上のソース画像へのアクセスをサポートします。

`src=` または `mask=` コマンドに外部 URL を指定するには、埋め込み URL 全体を中括弧で区切るだけです。

` …&src={ *[!DNL foreignUrl]*}&…`

完全な絶対 URL （`attribute::AllowDirectUrls` が設定されている場合）と、`attribute::RootUrl` を基準とした URL が許可されています。 絶対 URL が埋め込まれ、属性：`AllowDirectUrls` が 0 の場合、または相対 URL が指定され、`attribute::RootUrl` が空の場合は、エラーが発生します。

外部画像は、HTTP 応答に含まれるキャッシュヘッダーに従ってサーバーによってキャッシュされます。

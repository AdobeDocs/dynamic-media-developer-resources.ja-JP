---
title: 外部画像ソース
description: 画像サービングは、外部の HTTP および FTP サーバー上のソース画像へのアクセスをサポートします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# 外部画像ソース{#foreign-image-sources}

画像サービングは、外部の HTTP および FTP サーバー上のソース画像へのアクセスをサポートします。

の外部 URL を指定するには `src=` または `mask=` コマンド；埋め込み URL 全体を次の中括弧で区切ります。

` …&src={ *[!DNL foreignUrl]*}&…`

完全な絶対 URL ( `attribute::AllowDirectUrls` が設定されている ) と URL の相対値 `attribute::RootUrl` は許可されています。 絶対 URL が埋め込まれ、次の属性が含まれている場合は、エラーが発生します。 `AllowDirectUrls` が 0 の場合、または相対 URL が指定されている場合は `attribute::RootUrl` が空である。

外部画像は、HTTP 応答に含まれるキャッシュヘッダーに従って、サーバーによってキャッシュされます。

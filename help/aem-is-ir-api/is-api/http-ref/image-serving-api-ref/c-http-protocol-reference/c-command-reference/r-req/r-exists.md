---
description: 画像が存在します。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---

# 存在{#exists}

画像が存在します。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 一意のリクエスト ID

という名前の単一のプロパティを返します。 `catalogRecord.exists`. 指定したカタログエントリが画像またはデフォルトのカタログに存在する場合、プロパティ値は「1」に設定され、存在しない場合は「0」に設定されます。 `req=exists` に対する要求 `/is/content` context は、静的コンテンツカタログ内に指定したレコードが存在するかどうかを示します。

リクエスト文字列内の他のコマンドは無視されます。 HTTP 応答は、TTL に基づいてキャッシュ可能です。 `attribute::NonImgExpiration`.

JSONP 応答形式をサポートするリクエストでは、の拡張構文を使用して JS コールバックハンドラーの名前を指定できます。 `req=` パラメーター：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみ使用できます。 オプション。初期設定は `s7jsonResponse`.

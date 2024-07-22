---
description: 画像が存在する。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# 存在{#exists}

画像が存在する。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

一意 *`reqId`* リクエスト識別子

`catalogRecord.exists` という名前の 1 つのプロパティを返します。 指定したカタログエントリが画像またはデフォルトのカタログに存在する場合、プロパティ値は「1」に設定されます。存在しない場合は、「0」に設定されます。 `/is/content` コンテキストに対する `req=exists` リクエストは、静的コンテンツカタログ内の指定されたレコードの有無を示します。

リクエスト文字列内のその他のコマンドは無視されます。 HTTP 応答は、`attribute::NonImgExpiration` に基づく TTL でキャッシュ可能です。

JSONP 応答形式をサポートするリクエストでは、パラメーターの拡張構文を使用して JS コールバックハンドラーの名前 `req=` 指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみを使用できます。 オプション。 デフォルトは `s7jsonResponse` です。

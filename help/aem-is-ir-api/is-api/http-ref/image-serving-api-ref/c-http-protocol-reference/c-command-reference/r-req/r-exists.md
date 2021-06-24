---
description: 画像が存在します。
solution: Experience Manager
title: 存在
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# 存在{#exists}

画像が存在します。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 一意のリクエストID

`catalogRecord.exists`という名前の単一のプロパティを返します。 指定したカタログエントリが画像またはデフォルトのカタログに存在する場合、プロパティ値は「1」に設定され、それ以外の場合は「0」に設定されます。 `req=exists` コンテキストに対す `/is/content` るリクエストは、静的コンテンツカタログ内の指定されたレコードの有無を示します。

リクエスト文字列内の他のコマンドは無視されます。 HTTP応答は、`attribute::NonImgExpiration`に基づいてTTLでキャッシュ可能です。

JSONP応答形式をサポートするリクエストでは、 `req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

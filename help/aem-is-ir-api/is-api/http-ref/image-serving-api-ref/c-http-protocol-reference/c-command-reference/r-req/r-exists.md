---
description: 画像が存在します。
seo-description: 画像が存在します。
seo-title: 存在
solution: Experience Manager
title: 存在
topic: Scene7 Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# 存在{#exists}

画像が存在します。

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* 一意の要求識別子

`catalogRecord.exists`という名前の1つのプロパティを返します。 指定したカタログエントリが画像または初期設定のカタログに存在する場合、プロパティ値は「1」に設定され、それ以外の場合は「0」に設定されます。 `req=exists` コン `/is/content` テキストに対するリクエストは、静的コンテンツカタログ内の指定されたレコードの存在または存在を示します。

要求文字列内の他のコマンドは無視されます。 HTTP応答は、`attribute::NonImgExpiration`に基づいてTTLでキャッシュ可能です。

JSONP応答形式をサポートするリクエストでは、`req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

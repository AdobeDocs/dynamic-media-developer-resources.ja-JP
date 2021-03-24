---
description: 画像が存在します。
solution: Experience Manager
title: 存在
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

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

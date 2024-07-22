---
description: 画像カタログの画像セットデータ。 URL パスで指定された画像カタログエントリの画像セットデータを返します。
solution: Experience Manager
title: 画像セット
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# 画像セット{#imageset}

画像カタログの画像セットデータ。 URL パスで指定された画像カタログエントリの画像セットデータを返します。

`req=imageset[,text|javascript|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコーディング </span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

`catalog::ImageSet` のコンテンツは、それ以上の変更なしで返され（該当する場合は文字列のローカリゼーションを除く）、その後に 1 行の終端文字（CR/LF）が続きます。 URL パスが有効なカタログエントリに解決されない場合、応答は 1 行のターミネータのみで構成されます。

リクエスト文字列内のその他のコマンドは無視されます。 HTTP 応答は、`catalog::NonImgExpiration` に基づく TTL でキャッシュ可能です。

JSONP 応答形式をサポートするリクエストでは、パラメーターの拡張構文を使用して JS コールバックハンドラーの名前 `req=` 指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみを使用できます。 オプション。 デフォルトは `s7jsonResponse` です。

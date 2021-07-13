---
description: 画像カタログの画像セットデータ。 URLパスで指定された画像カタログエントリの画像セットデータを返します。
solution: Experience Manager
title: imageset
feature: Dynamic Media Classic,SDK/API，画像セット
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# imageset{#imageset}

画像カタログの画像セットデータ。 URLパスで指定された画像カタログエントリの画像セットデータを返します。

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

`catalog::ImageSet`の内容は、それ以降の変更(文字列のローカライゼーション（該当する場合）を除く)せずに返され、その後に1行の終端文字(CR/LF)が続きます。 URLパスが有効なカタログエントリに解決されない場合、応答は1行のターミネータのみで構成されます。

リクエスト文字列内の他のコマンドは無視されます。 HTTP応答は、`catalog::NonImgExpiration`に基づいてTTLでキャッシュ可能です。

JSONP応答形式をサポートするリクエストでは、 `req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

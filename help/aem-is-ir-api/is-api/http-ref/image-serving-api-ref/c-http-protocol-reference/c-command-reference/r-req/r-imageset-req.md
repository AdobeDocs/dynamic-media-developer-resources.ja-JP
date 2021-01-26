---
description: 画像カタログからの画像セットデータ。 URLパスで指定された画像カタログエントリの画像セットデータを返します。
seo-description: 画像カタログからの画像セットデータ。 URLパスで指定された画像カタログエントリの画像セットデータを返します。
seo-title: imageset
solution: Experience Manager
title: imageset
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# imageset{#imageset}

画像カタログからの画像セットデータ。 URLパスで指定された画像カタログエントリの画像セットデータを返します。

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>一意の要求識別子。 </p></td> 
 </tr> 
</table>

`catalog::ImageSet`の内容は、文字列ローカライゼーション（該当する場合）を変更せずに返され、その後に1行の終端文字(CR/LF)が続きます。 URLパスが有効なカタログエントリに解決されない場合、応答には1つの行終端子のみが含まれます。

要求文字列内の他のコマンドは無視されます。 HTTP応答は、`catalog::NonImgExpiration`に基づいてTTLでキャッシュ可能です。

JSONP応答形式をサポートするリクエストでは、`req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

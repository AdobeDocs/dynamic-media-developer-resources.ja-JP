---
description: 画像カタログの画像セットデータ。 URLパスで指定された画像カタログエントリの画像セットデータを返します。
seo-description: 画像カタログの画像セットデータ。 URLパスで指定された画像カタログエントリの画像セットデータを返します。
seo-title: imageset
solution: Experience Manager
title: imageset
topic: Scene7 Image Serving - Image Rendering API
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# imageset{#imageset}

画像カタログの画像セットデータ。 URLパスで指定された画像カタログエントリの画像セットデータを返します。

`req=imageset[,text|javascript|{xml[, *`encodingreqId`*]}|{json[&id= *``*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> エンコード</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>一意の要求識別子。 </p></td> 
 </tr> 
</table>

の内容は、それ `catalog::ImageSet` 以上変更を加えることなく返され（文字列のローカリゼーションが可能な場合は除く）、その後に1つの行終端文字(CR/LF)が続きます。 URLパスが有効なカタログエントリに解決されない場合、応答は1つの行終端文字のみで構成されます。

要求文字列内の他のコマンドは無視されます。 The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.

JSONP応答形式をサポートするリクエストを使用すると、次のパラメーターの拡張構文を使用してJSコールバックハンドラーの名前を指定で `req=` きます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。 a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

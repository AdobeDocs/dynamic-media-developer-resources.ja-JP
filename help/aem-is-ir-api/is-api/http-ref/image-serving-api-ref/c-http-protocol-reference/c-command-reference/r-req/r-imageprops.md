---
description: ソース画像のプロパティ。 URLパスで指定された画像ファイルまたはカタログエントリの選択されたプロパティを返します。
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 7%

---

# imageprops{#imageprops}

ソース画像のプロパティ。 URLパスで指定された画像ファイルまたはカタログエントリの選択されたプロパティを返します。

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

HTTP応答は、`attribute::NonImgExpiration`に基づいてTTLでキャッシュ可能です。

リクエスト文字列内の他のコマンドは無視されます。

JSONP応答形式をサポートするリクエストでは、 `req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

次のプロパティが返されます。

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> プロパティ</b> </td> 
   <td> <b> 種類</b> </td> 
   <td> <b> 説明</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> catalog::</span> デフォルトのアンカーポイントをアンカーします。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> 二重 </p> </td> 
   <td> <p> <span class="codeph"> catalog::</span> 有効期限またはデフォルトの有効期間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p>最大解像度の画像の高さ（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> この画像に関連付けられているプロファイルの名前/説明 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> イメージ. embeddedIccProfile</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 関連付けられたプロファイルが画像に埋め込まれている場合は1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 画像にPhotoshopパスデータが含まれる場合は1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> イメージ. embeddedXmpData</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 画像にXMPデータが含まれる場合は1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> マスクなしの場合は0、プリマルチプライアルファの場合は1、プリマルチプライアルファの場合は2、個別のマスクイメージの場合は3 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> catalog::</span> カタログエントリでない場合は空の値を変更 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> イメージ. photoshopPathNames</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> この画像に関連付けられているすべてのPhotoshopパスの名前のコンマ区切りリスト </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 画像タイプ。「CMYK」、「RGB」または「BW」（グレースケール画像の場合） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> attribute::</span> カタログエントリでない場合はPostModifieror empty </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> デフォルトの印刷解像度（ピクセル/インチ） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> catalog::</span> Resolutionまたはデフォルトのオブジェクト解像度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p>変更日時（<span class="codeph"> catalog::TimeStamp</span>または画像ファイルから） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> catalog::</span> ThumbResor初期設定のサムネール解像度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalog::</span> ThumbTypeまたは初期設定のサムネールの種類 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 最大解像度の画像の幅（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> パスで指定された<span class="varname">オブジェクト</span>の解決先となるカタログID（<a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local">オブジェクトIDの変換</a>を参照）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

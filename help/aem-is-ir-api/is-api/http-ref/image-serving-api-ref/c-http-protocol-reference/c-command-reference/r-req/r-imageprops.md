---
description: Sourceの画像プロパティ。 URL パスで指定された画像ファイルまたはカタログエントリの選択されたプロパティを返します。
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 4%

---

# imageprops{#imageprops}

Sourceの画像プロパティ。 URL パスで指定された画像ファイルまたはカタログエントリの選択されたプロパティを返します。

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p></td> 
 </tr> 
</table>

HTTP 応答は、`attribute::NonImgExpiration` に基づく TTL でキャッシュ可能です。

リクエスト文字列内のその他のコマンドは無視されます。

JSONP 応答形式をサポートするリクエストでは、パラメーターの拡張構文を使用して JS コールバックハンドラーの名前 `req=` 指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP 応答に存在する JS ハンドラーの名前です。 a ～ z、A ～ Z、0 ～ 9 文字のみを使用できます。 オプション。 デフォルトは `s7jsonResponse` です。

次のプロパティが返されます。

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> プロパティ </b> </td> 
   <td> <b> Type</b> </td> 
   <td> <b> Description</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> catalog::Anchor</span> またはデフォルトのアンカーポイント </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> 二重 </p> </td> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> またはデフォルトの有効期間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p>画像の高さ（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">.iccProfile</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> この画像に関連付けられているプロファイルの名前または説明 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 画像 <span class="codeph">。 embeddedIccProfile</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 関連付けられたプロファイルが画像に埋め込まれている場合は 1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 画像にPhotoshop パスデータが含まれている場合は 1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 画像 <span class="codeph">。 embeddedXmpData</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 画像にXMP データが含まれる場合は 1 を入力します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">.mask</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> マスクを適用しない場合は 0、事前合成アルファの場合は 1、事前合成されていないアルファの場合は 2、個別のマスク イメージの場合は 3 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> カタログエントリでない場合は空 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 画像 <span class="codeph">。 photoshopPathNames</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> この画像に関連付けられているすべてのPhotoshop パスの名前のコンマ区切りリスト </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 画像のタイプは、「CMYK」、「RGB」または「BW」（グレースケール画像用）にすることができます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">.postModifier</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> 属性：:PostModifier</span> またはカタログエントリでない場合は空 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> デフォルトの印刷解像度（ピクセル/インチ） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> またはデフォルトのオブジェクト解像度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">.timeStamp</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p>変更日時（カタログ：:TimeStamp<span class="codeph"> たは画像ファイル </span> ら） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbRes</span> またはデフォルトのサムネール解像度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">.thumbType</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbType</span> またはデフォルトのサムネールの種類 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">.width</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> フル解像度の画像の幅（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> パスで指定された <span class="varname"> オブジェクト </span> 解決されるカタログ ID （<a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> オブジェクト ID の変換を参照） </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

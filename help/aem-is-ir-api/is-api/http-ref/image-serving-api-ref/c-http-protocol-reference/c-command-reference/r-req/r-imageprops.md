---
description: ソース画像のプロパティ。 URLパスで指定された画像ファイルまたはカタログエントリの選択されたプロパティを返します。
seo-description: ソース画像のプロパティ。 URLパスで指定された画像ファイルまたはカタログエントリの選択されたプロパティを返します。
seo-title: imageprops
solution: Experience Manager
title: imageprops
topic: Scene7 Image Serving - Image Rendering API
uuid: e9bf2780-a520-4fb1-ab4c-40bb799e36a4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# imageprops{#imageprops}

ソース画像のプロパティ。 URLパスで指定された画像ファイルまたはカタログエントリの選択されたプロパティを返します。

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>一意の要求識別子。 </p></td> 
 </tr> 
</table>

The HTTP response is cacheable with the TTL based on `attribute::NonImgExpiration`.

要求文字列内の他のコマンドは無視されます。

JSONP応答形式をサポートするリクエストを使用すると、次のパラメーターの拡張構文を使用してJSコールバックハンドラーの名前を指定で `req=` きます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。 a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

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
   <td> <p> <span class="codeph"> catalog::Anchor</span> or the default anchor point </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> 二重 </p> </td> 
   <td> <p> <span class="codeph"> catalog::Expiration</span> 、または有効期限 </p> </td> 
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
   <td> <p> 関連するプロファイルが画像に埋め込まれている場合は1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 画像にPhotoshopのパスデータが含まれる場合は1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> イメージ. embeddedXmpData</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 画像にXMPデータが含まれる場合は1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> マスクなしの場合は0、乗算済みアルファの場合は1、乗算済みアルファの場合は2、個別のマスク画像の場合は3 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> catalog::Modifier</span> 、カタログエントリでない場合は空 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> イメージ. photoshopPathNames</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> この画像に関連付けられているすべてのPhotoshopパスの名前のコンマ区切りリスト </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 画像の種類。「CMYK」、「RGB」または「BW」（グレースケール画像の場合） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> attribute::PostModifier</span> （カタログエントリでない場合は空） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> 初期設定の印刷解像度（ピクセル/インチ） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> catalog::Resolution</span> or the default object resolution </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p>変更日時( <span class="codeph"> catalog::TimeStamp</span> 、または画像ファイルから) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbRes</span> 、または初期設定のサムネール解像度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbType</span> 、または初期設定のサムネールの種類 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 最大解像度画像の幅（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> パスで指定されたオブジェク <span class="varname"> トの</span> 解決先となるカタログID(オブジェクトIDの変 <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> 換を参照</a>)。 </p> </td> 
  </tr> 
 </tbody> 
</table>


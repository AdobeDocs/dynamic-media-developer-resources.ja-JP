---
description: 応答データのプロパティ。 現在の要求をイメージ要求(req=img)であるかのように評価しますが、イメージを返す代わりに、サーバーは、返信イメージの選択されたプロパティを返します。
seo-description: 応答データのプロパティ。 現在の要求をイメージ要求(req=img)であるかのように評価しますが、イメージを返す代わりに、サーバーは、返信イメージの選択されたプロパティを返します。
seo-title: prop
solution: Experience Manager
title: prop
topic: Scene7 Image Serving - Image Rendering API
uuid: b9325654-81d6-4f00-bf0a-36650bea6b8d
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 8%

---


# prop{#props}

応答データのプロパティ。 現在の要求をイメージ要求(req=img)であるかのように評価しますが、イメージを返す代わりに、サーバーは、返信イメージの選択されたプロパティを返します。

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId  </span> </span> </p> </td> 
  <td class="stentry"> <p>一意の要求識別子。 </p> </td> 
 </tr> 
</table>

JSONP応答形式をサポートするリクエストでは、`req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

応答の構文と応答のMIMEタイプについては、[プロパティ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)を参照してください。 HTTP応答は、`attribute::NonImgExpiration`に基づいてTTLでキャッシュ可能です。

/is/image要求に対して次のプロパティが返されます。

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> プロパティ</b> </td> 
   <td> <b> 種類</b> </td> 
   <td> <b> 説明</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> hex </p> </td> 
   <td> <p> 背景色（<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>を参照） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 返信画像の高さ（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> ICCプロファイルが返信画像に埋め込まれている場合はtrue。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像に関連付けられているプロファイルの名前/説明。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length  </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> HTTPヘッダーを含まないピクセル単位の応答サイズ。0は、応答画像データがサーバーによって以前にキャッシュされていない場合に発生します。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> 返信画像にアルファチャネルが含まれる場合は1、それ以外の場合は0。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像の種類（<span class="codeph"> CMYK </span>、<span class="codeph"> RGB </span>または<span class="codeph"> BW </span>）（グレースケール画像の場合）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 応答画像にパスが埋め込まれている場合は1、それ以外の場合は0。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> 印刷解像度(dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> JPEG画質 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像のMIMEタイプ。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 返信画像の幅（ピクセル単位） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed  </span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 応答画像がxmpデータを埋め込む場合は1、それ以外の場合は0。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version  </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 画像のバージョン識別子。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version  </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> メタデータのバージョン識別子。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>を参照）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`/is/content`要求に対して次のプロパティが返されます。

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> プロパティ</b> </td> 
   <td> <b> 種類</b> </td> 
   <td> <b> 説明</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> パス </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p>部分的に解決されたファイルのパス。 （「<span class="codeph"> static::Path </span>」を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> length </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> オブジェクトファイルのサイズ（バイト） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 有効期限 </span> </p> </td> 
   <td> <p> 二重 </p> </td> 
   <td> <p> <span class="codeph"> static::Expiration </span> またはデフォルトの有効期間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified  </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 変更日時（<span class="codeph"> static::TimeStamp </span>またはオブジェクトファイルから） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType  </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> static::UserType  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>


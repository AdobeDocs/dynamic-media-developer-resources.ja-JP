---
description: 応答データのプロパティ。 現在の要求を画像要求(req=img)として評価しますが、画像を返す代わりに、サーバーは返信画像の選択されたプロパティを返します。
solution: Experience Manager
title: prop
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 8%

---

# prop{#props}

応答データのプロパティ。 現在の要求を画像要求(req=img)として評価しますが、画像を返す代わりに、サーバーは返信画像の選択されたプロパティを返します。

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId  </span> </span> </p> </td> 
  <td class="stentry"> <p>一意のリクエスト識別子。 </p> </td> 
 </tr> 
</table>

JSONP応答形式をサポートするリクエストでは、 `req=`パラメーターの拡張構文を使用して、JSコールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` は、JSONP応答に存在するJSハンドラーの名前です。a ～ z、A ～ Zおよび0 ～ 9文字のみ使用できます。 （オプション）初期設定は `s7jsonResponse`.

応答の構文と応答のMIMEタイプの説明については、[プロパティ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)を参照してください。 HTTP応答は、`attribute::NonImgExpiration`に基づいてTTLでキャッシュ可能です。

/is/imageリクエストに対して、次のプロパティが返されます。

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
   <td> <p> 背景色（ <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>を参照） </p> </td> 
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
   <td> <p> HTTPヘッダーを含まない応答サイズ（ピクセル単位）。0 ：返信画像データがサーバーによって以前にキャッシュされていない場合。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 1 ：返信画像にアルファチャンネルが含まれる場合は1、それ以外の場合は0。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixType  </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像のタイプ。CMYK </span>、<span class="codeph"> RGB </span>または<span class="codeph"> BW </span>（グレースケール画像の場合）を使用できます。<span class="codeph"> </span></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 応答画像に任意のパスが埋め込まれる場合は1、それ以外の場合は0。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>を参照）。 </p> </td> 
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
   <td> <p> 応答画像にxmpデータが埋め込まれる場合は1、それ以外の場合は0。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>を参照）。 </p> </td> 
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

`/is/content`リクエストに対して、次のプロパティが返されます。

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
   <td> <p>部分的に解決されたファイルパス。 （<span class="codeph"> static::Path </span>を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> length </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> オブジェクトファイルのサイズ（バイト単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 有効期限 </span> </p> </td> 
   <td> <p> 二重 </p> </td> 
   <td> <p> <span class="codeph"> static:：有効期 </span> 限またはデフォルトの有効期間 </p> </td> 
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

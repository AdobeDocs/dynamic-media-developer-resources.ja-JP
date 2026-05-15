---
description: 応答データプロパティ： 現在のリクエストを画像リクエスト （req=img）であるかのように評価しますが、画像を返す代わりに、サーバーは返信画像の選択したプロパティを返します。
solution: Experience Manager
title: prop
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
TQID: 'https://experienceleague.adobe.com/grTKxMVRKQ8-casDC-aGK6xeQQwqsg2sRLRBGlTrXdc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 373
ht-degree: 5%

---

# prop{#props}

応答データプロパティ： 現在のリクエストを画像リクエスト （req=img）であるかのように評価しますが、画像を返す代わりに、サーバーは返信画像の選択したプロパティを返します。

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">件のreqId </span> </span> </p> </td> 
  <td class="stentry"> <p>一意のリクエスト ID。 </p> </td> 
 </tr> 
</table>

JSONP応答形式をサポートするリクエストでは、`req=` パラメーターの拡張構文を使用してJS コールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`は、JSONP応答に存在するJS ハンドラーの名前です。 a ～ z、A ～ Z、および0 ～ 9文字のみ使用できます。 オプション。 デフォルトは`s7jsonResponse`です。

返信構文と応答MIME タイプの説明については、[ プロパティ ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)を参照してください。 HTTP応答は、`attribute::NonImgExpiration`に基づくTTLでキャッシュできます。

/is/image リクエストに対して次のプロパティが返されます。

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> プロパティ </b> </td> 
   <td> <b> タイプ </b> </td> 
   <td> <b>説明</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> 16進 </p> </td> 
   <td> <p> 背景色（<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 画像の高さをピクセル単位で返信 </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 返信画像にICC プロファイルが埋め込まれている場合はTrueです。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像に関連付けられているプロファイルの名前/説明。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 返信画像データがサーバーによって以前にキャッシュされていない場合は、HTTP ヘッダーを含まないピクセル単位の返信数サイズ。0。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> 返信画像にアルファチャンネルが含まれる場合は1、それ以外の場合は0です。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像タイプは、<span class="codeph"> CMYK </span>、<span class="codeph"> RGB </span>または<span class="codeph"> BW </span>です（グレースケール画像の場合）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 応答イメージにパスが埋め込まれている場合は1、それ以外の場合は0です。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> 印刷解像度（dpi） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> JPEGの品質。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 返信画像のMIME タイプ。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 画像の幅をピクセル単位で返信します。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed </span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 1応答イメージにxmp データが埋め込まれている場合は0、それ以外の場合は0。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 画像のバージョン識別子。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>を参照）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> メタデータのバージョン識別子。 （<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>を参照）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`/is/content`要求に対して、次のプロパティが返されます。

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> プロパティ </b> </td> 
   <td> <b> タイプ </b> </td> 
   <td> <b>説明</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> パス </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p>部分的に解決されたファイルパス。 （<span class="codeph">静的：：パス </span>を参照）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">長さ</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> オブジェクトファイルサイズ（バイト単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">有効期限</span> </p> </td> 
   <td> <p> 二重 </p> </td> 
   <td> <p> <span class="codeph">静的：：有効期限</span>またはデフォルトの有効期間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">最終変更日：</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 変更日時（<span class="codeph">静的：:TimeStamp </span>またはオブジェクトファイルから） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType </span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph">静的：:UserType </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

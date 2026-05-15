---
description: Sourceの画像プロパティ： URL パスで指定された画像ファイルまたはカタログエントリの選択したプロパティを返します。
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
TQID: 'https://experienceleague.adobe.com/idRlUDsoqYYoak6kMyqn9-IeJHBShjjqaHvtDKgRUhw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 340
ht-degree: 5%

---

# imageprops{#imageprops}

Sourceの画像プロパティ： URL パスで指定された画像ファイルまたはカタログエントリの選択したプロパティを返します。

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>一意のリクエスト ID。 </p></td> 
 </tr> 
</table>

HTTP応答は、`attribute::NonImgExpiration`に基づくTTLでキャッシュできます。

リクエスト文字列内のその他のコマンドは無視されます。

JSONP応答形式をサポートするリクエストでは、`req=` パラメーターの拡張構文を使用してJS コールバックハンドラーの名前を指定できます。

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`は、JSONP応答に存在するJS ハンドラーの名前です。 a ～ z、A ～ Z、および0 ～ 9文字のみ使用できます。 オプション。 デフォルトは`s7jsonResponse`です。

次のプロパティが返されます。

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> プロパティ </b> </td> 
   <td> <b> タイプ </b> </td> 
   <td> <b>説明</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> カタログ：：アンカー</span>または既定のアンカーポイント </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> 二重 </p> </td> 
   <td> <p> <span class="codeph"> カタログ：：有効期限</span>または既定の有効期間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p>フル解像度の画像の高さ（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> この画像に関連付けられているプロファイルの名前/説明 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">画像。 embeddedIccProfile</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 1関連するプロファイルが画像に埋め込まれている場合 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 1画像にPhotoshop path dataが含まれている場合 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">画像。 embeddedXmpData</span> </p> </td> 
   <td> <p> ブール </p> </td> 
   <td> <p> 1画像にXMP データが含まれている場合 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> マスクなし場合は0、事前乗算済みアルファの場合は1、非乗算済みアルファの場合は2、個別のマスク画像の場合は3です </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph"> カタログ：：修飾子</span>またはカタログ エントリでない場合は空 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">画像。 photoshopPathNames</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> この画像に関連付けられているすべてのPhotoshop パスの名前をコンマ区切りのリスト </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> 画像の種類。CMYK、RGB、BWのいずれかです（グレースケール画像の場合） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> <span class="codeph">属性：:PostModifier</span>またはカタログエントリでない場合は空 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> デフォルトの印刷解像度（ピクセル/インチ） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> カタログ：:Resolution</span>または既定のオブジェクト解決 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p>変更日時（<span class="codeph"> カタログ：:TimeStamp</span>または画像ファイルから） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> 真の </p> </td> 
   <td> <p> <span class="codeph"> カタログ：:ThumbRes</span>または既定のサムネール解決 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> <span class="codeph"> カタログ：:ThumbType</span>または既定のサムネールの種類 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> フル解像度の画像幅（ピクセル単位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> 文字列 </p> </td> 
   <td> <p> パスで指定された<span class="varname"> オブジェクト </span>が解決されるカタログ ID （<a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> オブジェクト ID翻訳</a>を参照）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

---
title: bgColor
description: レイヤーの背景色。 現在のレイヤーの背景色と不透明度を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 22c957e6-1a82-43a7-8467-871a150e7453
TQID: 'https://experienceleague.adobe.com/lpjSBEeFr3Vqd2d8ab98fO0uie4jENOumXwyg6PQP64'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 4%

---

# bgColor{#bgcolor}

レイヤーの背景色。 現在のレイヤーの背景色と不透明度を指定します。

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> カラー</span></span> </p> </td> 
  <td class="stentry"> <p>アルファの有無にかかわらず、グレー、RGB、またはCMYK カラー値。 </p></td> 
 </tr> 
</table>

レイヤーのバウンディング矩形内の透明な領域と半不透明な領域は、* `opac=`、`rotate=`、`extend=`を適用した後、指定した色*で塗りつぶされます。

## プロパティ {#section-19dfc13e997f4a33889a1df1e4ad50b9}

レイヤー属性。 現在のレイヤーまたは`layer=comp`のレイヤー0に適用されます。 エフェクトレイヤーでは無視されます。

*`color`*&#x200B;は、*`color`*&#x200B;のピクセルタイプに対応する作業用カラースペースに存在すると想定されます。 最終レイヤー画像のピクセルタイプが異なる場合、*`color`*&#x200B;は正確に変換されます。

## 初期設定 {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0 （完全に透明）。

## 例 {#section-6e14fcf1d31e432dbdb56b9320904453}

[color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)を参照してください。

## 関連項目 {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)、[color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)、[blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172)、[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)、[extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)、[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)、[bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)、[ カラーマネジメント ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)

---
title: 切り抜き
description: 画像を切り抜く： 長方形の切り抜き領域を指定します。ピクセル単位で表示するか、全解像度のソースイメージまたはマスクイメージを基準にして正規化します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
TQID: 'https://experienceleague.adobe.com/sFmHyBwHZcqIxp9LWE8IphN3RCa-auGEph0WbFzs1n0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 1%

---

# 切り抜き{#crop}

画像を切り抜く： 長方形の切り抜き領域を指定します。ピクセル単位で表示するか、全解像度のソースイメージまたはマスクイメージを基準にして正規化します。

`crop= *` コード `*, *` サイズ `*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> コード </span></span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上隅から切り抜きレクトの左上隅までのピクセルオフセット（int、int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上から切り抜きレクトの左上への正規化されたオフセット（実際、実際）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> サイズ </span></span> </p></td> 
  <td class="stentry"> <p>切り抜きレクトのサイズ （ピクセル単位、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>ソース画像のサイズ（実際、実際）に対する切り抜きレクトの正規化されたサイズ。 </p></td> 
 </tr> 
</table>

また、負のx、y値および/または幅、画像の幅よりも大きい高さ値、高さ値を指定して、画像の境界を超えて画像を拡張するために使用することもできます。 この場合、拡張エリアは完全に透明になります（`bgColor=`が指定されていない限り）。

## プロパティ {#section-632e0405bb9940679b5f8b1c10e0902e}

Source image/mask属性。 `layer=comp`の場合、レイヤー0のソース画像に適用されます。 ソース画像またはマスクに関連付けられていないレイヤーによって無視されます。

## 初期設定 {#section-41f62d386c664f77952bc22e7286bb88}

画像全体（`cropN=0,0,1,1`）。

## 例 {#section-2c99b481c0a04321979a3b522aa295d1}

**左から10%、右から10%の切り抜き：**

`…&cropN=0.1,0,0.8,1&…`

**画像の下端から20%切り抜き：**

`…&cropN=0,0,1,0.8&…`

## 関連項目 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)、[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)、[extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)

---
description: 画像の切り抜き 長方形の切り抜き領域をピクセル単位で指定するか、最大解像度のソース画像またはマスク画像を基準にして正規化します。
seo-description: 画像の切り抜き 長方形の切り抜き領域をピクセル単位で指定するか、最大解像度のソース画像またはマスク画像を基準にして正規化します。
seo-title: 切り抜き
solution: Experience Manager
title: 切り抜き
topic: Scene7 Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 切り抜き{#crop}

画像の切り抜き 長方形の切り抜き領域をピクセル単位で指定するか、最大解像度のソース画像またはマスク画像を基準にして正規化します。

`crop= *`正`*, *`規`*`

`cropN= *`coordNsizeN`*, *``*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 心</span></span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上隅から切り抜き領域の左上隅（整数、整数）までのピクセルオフセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> coordN <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上から切り抜き領域の左上への正規化されたオフセット（実数、実数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 大きさ</span></span> </p></td> 
  <td class="stentry"> <p>切り抜き領域のサイズ（ピクセル単位、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> サイ <span class="varname"> ズN</span></span> </p></td> 
  <td class="stentry"> <p>ソース画像のサイズを基準とした切り抜き領域の正規化サイズ（実数、実数）。 </p></td> 
 </tr> 
</table>

また、x、yの負の値や幅、画像の幅、高さより大きい値を指定して、画像を境界を越えて拡張する場合にも使用できます。 この場合、拡張領域は完全に透明になります(が指定されて `bgColor=` いない場合)。

## プロパティ {#section-632e0405bb9940679b5f8b1c10e0902e}

ソース画像/マスク属性。 レイヤー0のソース画像（の場合）に適用しま `layer=comp`す。 ソース画像またはマスクに関連付けられていないレイヤーでは無視されます。

## 初期設定 {#section-41f62d386c664f77952bc22e7286bb88}

画像全体( `cropN=0,0,1,1`)

## 例 {#section-2c99b481c0a04321979a3b522aa295d1}

**切り抜き（左から10%、右から10%）:**

`…&cropN=0.1,0,0.8,1&…`

**画像の下端から20%切り抜き：**

`…&cropN=0,0,1,0.8&…`

## 関連項目 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)

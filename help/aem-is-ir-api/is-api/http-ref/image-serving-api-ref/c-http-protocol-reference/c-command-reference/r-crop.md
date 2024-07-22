---
title: 切り抜き
description: 画像を切り抜きます。 長方形の切り抜き領域をピクセル単位で指定するか、フル解像度のソース画像またはマスク画像を基準に正規化します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# 切り抜き{#crop}

画像を切り抜きます。 長方形の切り抜き領域をピクセル単位で指定するか、フル解像度のソース画像またはマスク画像を基準に正規化します。

`crop= *`coord`*, *`size`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上隅から切り抜き長方形の左上へのピクセルオフセット （int、int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上から切り抜き矩形の左上（実際、実際）までの正規化されたオフセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> サイズ </span></span> </p></td> 
  <td class="stentry"> <p>切り抜き矩形のサイズ （ピクセル単位） （整数、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>ソース画像のサイズ（実際、実際）に対して最近の切り抜きの正規化されたサイズ。 </p></td> 
 </tr> 
</table>

x、y、幅（負の値）、画像の幅より大きい高さ、高さを指定して、画像を境界を超えて拡張する場合にも使用できます。 この場合、拡張領域は完全に透明になります（`bgColor=` が指定されていない場合）。

## プロパティ {#section-632e0405bb9940679b5f8b1c10e0902e}

Source image/mask 属性。 レイヤー 0 のソース画像に適用されます（`layer=comp` の場合）。 ソース イメージまたはマスクに関連付けられていないレイヤによって無視されます。

## 初期設定 {#section-41f62d386c664f77952bc22e7286bb88}

画像全体（`cropN=0,0,1,1`）。

## 例 {#section-2c99b481c0a04321979a3b522aa295d1}

**左側を 10% オフ、右側を 10% オフに切り抜く：**

`…&cropN=0.1,0,0.8,1&…`

**画像の下端から 20% 切り抜く：**

`…&cropN=0,0,1,0.8&…`

## 関連項目 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)、[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)、[extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)

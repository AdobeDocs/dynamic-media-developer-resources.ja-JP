---
title: 切り抜き
description: 画像を切り抜く。 最大解像度のソース画像またはマスク画像を基準に、ピクセル単位で、または正規化された長方形の切り抜き領域を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# 切り抜き{#crop}

画像を切り抜く。 最大解像度のソース画像またはマスク画像を基準に、ピクセル単位で、または正規化された長方形の切り抜き領域を指定します。

`crop= *`コード`*, *`サイズ`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> コード</span></span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上隅から切り抜き範囲の左上端までのピクセルオフセット（整数、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上から切り抜き領域の左上（実数、実数）への正規化されたオフセット。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> サイズ</span></span> </p></td> 
  <td class="stentry"> <p>切り抜きの正確なサイズ（ピクセル単位、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>ソース画像のサイズを基準とした切り抜き領域の正規化サイズ（実数、実数）。 </p></td> 
 </tr> 
</table>

また、x、y の負の値や幅、画像の幅、高さよりも大きい値を指定することで、画像の境界を越えて画像を拡張する場合にも使用できます。 この場合、拡張領域は完全に透明です ( `bgColor=` を指定した場合 )。

## プロパティ {#section-632e0405bb9940679b5f8b1c10e0902e}

ソース画像/マスクの属性。 次の場合に、レイヤ 0 のソース画像に適用されます。 `layer=comp`. ソース画像またはマスクに関連付けられていないレイヤーでは無視されます。

## 初期設定 {#section-41f62d386c664f77952bc22e7286bb88}

画像全体 ( `cropN=0,0,1,1`) をクリックします。

## 例 {#section-2c99b481c0a04321979a3b522aa295d1}

**左から 10%、右から 10%切り抜き：**

`…&cropN=0.1,0,0.8,1&…`

**画像の下端から 20%ずつ切り抜く：**

`…&cropN=0,0,1,0.8&…`

## 関連項目 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)

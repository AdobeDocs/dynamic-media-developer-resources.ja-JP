---
description: レイヤーの背景色 現在のレイヤーの背景色と不透明度を指定します。
seo-description: レイヤーの背景色 現在のレイヤーの背景色と不透明度を指定します。
seo-title: bgColor
solution: Experience Manager
title: bgColor
topic: Scene7 Image Serving - Image Rendering API
uuid: bcbd368f-d200-4b1f-8e9f-bf4d88f14b72
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgColor{#bgcolor}

レイヤーの背景色 現在のレイヤーの背景色と不透明度を指定します。

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 色</span></span> </p> </td> 
  <td class="stentry"> <p>グレー、RGBまたはCMYKのカラー値（アルファ付き、アルファなし）。 </p></td> 
 </tr> 
</table>

レイヤーのバウンディング長方形内の透明な領域と半不透明な領域は、*の後に*を付けて指定した色で塗りつぶさ `opac=`れ、* `rotate=`が適用 `extend=` されます。

## プロパティ {#section-19dfc13e997f4a33889a1df1e4ad50b9}

レイヤー属性。 現在の画層または画層0（場合）に適用されま `layer=comp`す。 エフェクトレイヤーでは無視されます。

*`color`* は、のピクセルタイプに対応する作業用カラースペースに存在すると見なされま *`color`*&#x200B;す。 *`color`* は、最終的なレイヤー画像のピクセルタイプが異なる場合、正確に変換されます。

## 初期設定 {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0（完全に透明）

## 例 {#section-6e14fcf1d31e432dbdb56b9320904453}

color=を参 [照してくださ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)い。

## 関連項目 {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423), [blendMode=,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172)opac= [opac,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)extend=otate, [rotate,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[lotate, bgc=on, color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)

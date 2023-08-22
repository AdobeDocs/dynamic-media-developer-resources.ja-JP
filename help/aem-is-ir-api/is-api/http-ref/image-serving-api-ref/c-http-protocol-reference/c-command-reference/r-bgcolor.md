---
title: bgColor
description: レイヤーの背景色 現在のレイヤーの背景色と不透明度を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 22c957e6-1a82-43a7-8467-871a150e7453
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# bgColor{#bgcolor}

レイヤーの背景色 現在のレイヤーの背景色と不透明度を指定します。

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> カラー</span></span> </p> </td> 
  <td class="stentry"> <p>グレー、RGB、CMYK のカラー値（アルファ付き、またはアルファなし）。 </p></td> 
 </tr> 
</table>

レイヤーのバウンディング長方形内の透明な領域と半不透明な領域は、*後に指定した色で塗りつぶされます。 `opac=`, `rotate=`、および `extend=` が適用されます。

## プロパティ {#section-19dfc13e997f4a33889a1df1e4ad50b9}

レイヤー属性。 現在の画層に適用され、次の場合は画層 0 に適用されます `layer=comp`. 効果画層で無視されます。

*`color`* は、 *`color`*. *`color`* 最終的なレイヤーイメージのピクセルタイプが異なる場合、は正確に変換されます。

## 初期設定 {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0 （完全に透明）。

## 例 {#section-6e14fcf1d31e432dbdb56b9320904453}

詳しくは、 [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## 関連項目 {#section-64b3f153c6d94ab58f46e77324697818}

[カラー](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423), [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [カラーマネジメント](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)

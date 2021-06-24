---
description: 画像をビューに合わせる wid=とhei=で定義されたビューの長方形内で、合成画像を揃えます（scl=が指定されている場合も、拡大・縮小後に配置します）。
solution: Experience Manager
title: align
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---

# align{#align}

画像をビューに合わせる wid=とhei=で定義されたビューの長方形内で、合成画像を揃えます（scl=が指定されている場合も、拡大・縮小後に配置します）。

` align= *``*, *`水平`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz  </span> </span> </p> </td> 
  <td class="stentry"> <p>水平方向の整列（実数、-1.0 ～ 1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert  </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直方向の整列（実数、-1.0 ～ 1.0） </p> </td> 
 </tr> 
</table>

`align=-1,-1`を指定して合成画像の左上をビューの左上に揃え、`align=1,1`を指定して画像の右下をビューの右下に揃えます。 標準の画像要求およびサムネール要求の場合、合成画像データで覆われていないビューの領域は`bgc=`で埋められます。

## プロパティ {#section-3fbec8206fc944eda4746d8be84f3b41}

属性を表示します。 （ `align=`は、透かし画像と透かしが適用される合成画像の間の配置を定義する場合にも使用されます）。 現在の画層設定に関係なく適用されます。 `wid=`と`hei=`のいずれか1つのみが指定され、`fit=constrain`または`fit=stretch`の場合は無視されます。

## 初期設定 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`：画像をビューの長方形の中央に配置します。

## 例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

次のリクエストは、200 x 200ピクセルのビュー長方形に`myImage`適合します。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

`myImage`が正方形の場合、ビューの長方形全体が塗りつぶされます。 `myImage`の縦横比が縦長の場合は、縦200ピクセルに拡大縮小され、ビューの水平方向に中央揃えされます。 `myImage`の縦横比が横長の場合は、幅が200ピクセルに拡大縮小され、ビューの上端に合わせて整列されます。 どの場合でも、返される画像のサイズは正確に200 x 200ピクセルです。スケール`myImage`で覆われていないスペースは`attribute::BkgColor`で埋められます（背景色を動的に制御するにはbgc=を指定します）。

## 関連項目 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 、 [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、 [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)、 [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)、 [透かし](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)

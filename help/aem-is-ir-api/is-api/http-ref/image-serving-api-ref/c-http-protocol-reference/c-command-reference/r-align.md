---
title: 整列
description: 画像をビューに合わせる。 wid=とhei=で定義されたビュー長方形の中に合成画像を整列させます（scl=が指定されている場合は、拡大縮小した後に行うこともできます）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
TQID: 'https://experienceleague.adobe.com/ZIogqM83I6NCYf8tQkCPuGDfhxZPq9aQXcgW4xR2lJE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 1%

---

# 整列{#align}

画像をビューに合わせる。 wid=とhei=で定義されたビュー長方形の中に合成画像を整列させます（scl=が指定されている場合は、拡大縮小した後に行うこともできます）。

` align= *`horiz`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span> </span> </p> </td> 
  <td class="stentry"> <p>水平方向の整列（実数、-1.0...1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直方向の整列（実数、-1.0...1.0） </p> </td> 
 </tr> 
</table>

`align=-1,-1`を指定して、合成画像の左上をビューの左上に揃え、`align=1,1`を指定して、画像の右下をビューの右下に揃えます。 標準画像およびサムネール要求の場合、合成画像データでカバーされていないビューの領域は`bgc=`で塗りつぶされます。

## プロパティ {#section-3fbec8206fc944eda4746d8be84f3b41}

ビュー属性。 （`align=`は、透かし画像と、透かしを適用する合成画像との整合性を定義するためにも使用されます）。 現在のレイヤー設定に関係なく適用されます。 `wid=`と`hei=`のうち1つしか指定されていない場合と、`fit=constrain`または`fit=stretch`の場合は無視されます。

## 初期設定 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`。ビューの長方形に画像を中央に配置します。

## 例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

次のリクエストは、`myImage`を200 x 200 ピクセル ビューの長方形に適合させます。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

`myImage`が正確に正方形の場合、ビューの長方形全体が塗りつぶされます。 `myImage`に縦横比がある場合、縦横比は200 ピクセルに拡大/縮小され、ビュー内で水平方向に中央に配置されます。 `myImage`の縦横比が横長の場合、縦横比は200 ピクセル幅に拡大/縮小され、ビューの上端に揃えられます。 いずれの場合も、返される画像のサイズは正確に200 x 200 ピクセルです。拡大・縮小された`myImage`でカバーされていないスペースには`attribute::BkgColor`が表示されます（背景色を動的に制御するにはbgc=を指定してください）。

## 関連項目 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、[fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)、[bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)、[透かし](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)

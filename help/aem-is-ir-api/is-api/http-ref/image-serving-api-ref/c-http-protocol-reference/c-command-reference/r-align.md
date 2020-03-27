---
description: 画像をビューに揃える wid=とhei=で定義されたビューの長方形内で、合成画像を（拡大・縮小後も、scl=が指定されている場合は）揃えます。
seo-description: 画像をビューに揃える wid=とhei=で定義されたビューの長方形内で、合成画像を（拡大・縮小後も、scl=が指定されている場合は）揃えます。
seo-title: align
solution: Experience Manager
title: align
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# align{#align}

画像をビューに揃える wid=とhei=で定義されたビューの長方形内で、合成画像を（拡大・縮小後も、scl=が指定されている場合は）揃えます。

` align= *`水平`*, *`線`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 水平 </span></span> </p> </td> 
  <td class="stentry"> <p>水平方向の位置揃え（実数、-1.0 ～ 1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 背 </span> 面 </span> </p> </td> 
  <td class="stentry"> <p>垂直方向の位置揃え（実数、-1.0 ～ 1.0） </p> </td> 
 </tr> 
</table>

合成 `align=-1,-1` 画像の左上をビューの左上に揃える場合に指定し、画像の右下をビューの右下に揃え `align=1,1` る場合に指定します。 標準的な画像およびサムネールの要求の場合、合成画像データで覆われていないビューの領域は塗りつぶされま `bgc=`す。

## プロパティ {#section-3fbec8206fc944eda4746d8be84f3b41}

属性を表示します。 (透か `align=` し画像と、透かしを適用する合成画像との間の位置を定義する場合にも使用します)。現在のレイヤー設定に関係なく適用されます。 とのいずれか1つのみが指定され、 `wid=` また `hei=` はが指定された場合は無 `fit=constrain` 視されま `fit=stretch`す。

## 初期設定 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`ビューの長方形の中央に画像を配置します。

## 例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

次の要求は、200 x 200ピク `myImage` セルのビュー長方形に収まります。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

が正 `myImage` 確に正方形の場合、ビューの長方形全体を埋めます。 縦長 `myImage` の縦横比の場合は、高さが200ピクセルになり、ビューの水平方向の中央に配置されます。 横長 `myImage` の縦横比の場合、幅が200ピクセルに調整され、ビューの上端に揃えられます。 いずれの場合も、返される画像のサイズはちょうど200 x 200ピクセルです。拡大・縮小されていないスペースは `myImage` 満たされます( `attribute::BkgColor` 背景色を動的に制御するには、bgc=を指定します)。

## 関連項目 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , hei= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)fit= [, bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[watermarks](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)

---
description: 画像を表示に揃える wid=およびhei=で定義されている表示の長方形内で、合成画像を（拡大/縮小後に、scl=も指定した場合に）揃えます。
seo-description: 画像を表示に揃える wid=およびhei=で定義されている表示の長方形内で、合成画像を（拡大/縮小後に、scl=も指定した場合に）揃えます。
seo-title: align
solution: Experience Manager
title: align
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 1%

---


# align{#align}

画像を表示に揃える wid=およびhei=で定義されている表示の長方形内で、合成画像を（拡大/縮小後に、scl=も指定した場合に）揃えます。

` align= *``*, *`水平`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz  </span> </span> </p> </td> 
  <td class="stentry"> <p>水平方向の位置揃え（実数、-1.0 ～ 1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert  </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直方向の位置揃え（実数、-1.0 ～ 1.0） </p> </td> 
 </tr> 
</table>

合成画像の左上を表示の左上に揃えるには`align=-1,-1`を指定し、画像の右下を表示の右下に揃えるには`align=1,1`を指定します。 標準的な画像とサムネール要求に対しては、表示の中で、合成画像データの対象とならない領域は`bgc=`で埋められます。

## プロパティ {#section-3fbec8206fc944eda4746d8be84f3b41}

表示属性。 （`align=`は、透かし画像と、透かしを適用する合成画像の位置を定義するためにも使用されます）。 現在のレイヤー設定に関係なく適用されます。 `wid=`と`hei=`のいずれか1つのみが指定され、`fit=constrain`または`fit=stretch`の場合は無視されます。

## 初期設定 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`を指定すると、画像が表示の長方形の中央に配置されます。

## 例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

次のリクエストは、`myImage`を200 x 200ピクセルの表示の長方形に収めます。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

`myImage`が正方形の場合は、表示の長方形全体を占めます。 `myImage`が縦長の縦横比の場合は、高さが200ピクセルになるように拡大縮小され、表示の水平方向に中央揃えされます。 `myImage`の縦横比が横長の場合は、幅が200ピクセルになり、表示の上端に合わせて調整されます。 いずれの場合も、返される画像のサイズはちょうど200 x 200ピクセルです。スケール`myImage`で覆われていないスペースは、`attribute::BkgColor`で埋められます（背景色を動的に制御するには、bgc=を指定します）。

## 関連項目 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), bgc= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [watermarks](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)

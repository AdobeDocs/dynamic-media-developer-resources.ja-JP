---
description: レイヤーを拡張 レイヤーに余白を追加するか、レイヤーの長方形をトリミングします。
seo-description: レイヤーを拡張 レイヤーに余白を追加するか、レイヤーの長方形をトリミングします。
seo-title: 延長する
solution: Experience Manager
title: 延長する
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ca69994-e788-41a9-93ac-f22b6b9920d0
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 延長する{#extend}

レイヤーを拡張 レイヤーに余白を追加するか、レイヤーの長方形をトリミングします。

`extend= *`lefttoprightbottom`*, *``*, *``*, *``*`

`extendN= *`leftNtopNrightNbottomN`*, *``*, *``*, *``*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> left,top,bottom,right</span></span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの左端、上端、右端および下端(int、int、int、int)に追加（負の値の場合は削除）するピクセル数です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの左端、上端、右端および下端に追加（負の値の場合は削除）するスペースの量。元のレイヤーrectのサイズ(real、real、real、real、real)を基準とした正規化された量で表されます。 </p></td> 
 </tr> 
</table>

`extend=` は、画像が切り抜かれ ** ()、を含むすべてのレイ `crop=`ヤー変換が適用された後に、レイヤー `rotate=`に適用されます。

拡張領域は塗りつぶされ、指定し `bgColor=`なかった場合は透明のままになります。

の引数値は、レ `extendN=` イヤー変換後のレイヤーrectのサイズを基準にして正規化されます。このサイズには、適用済 `rotate=` みも含まれます。

## プロパティ {#section-8fc94de871f841f3bf5e1df135972ca9}

レイヤー属性。 レイヤー0の場合に適用されま `layer=comp`す。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`（レイヤーの長方形は変更されません）。

## 例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**画像を切り抜き、5ピクセル幅の赤い境界線を追加します。**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**画像の幅を200ピクセルに調整し、画像の上の30ピクセルの余白にタイトルテキストを追加します。**

合成画像の高さは、画像の縦横比によって異なります。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 関連項目 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)

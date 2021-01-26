---
description: レイヤーを拡張 マージンをレイヤーに追加するか、レイヤーの長方形をトリミングします。
seo-description: レイヤーを拡張 マージンをレイヤーに追加するか、レイヤーの長方形をトリミングします。
seo-title: 延長する
solution: Experience Manager
title: 延長する
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7ca69994-e788-41a9-93ac-f22b6b9920d0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# 拡張{#extend}

レイヤーを拡張 マージンをレイヤーに追加するか、レイヤーの長方形をトリミングします。

`extend= *``*, *``*, *``*, *`lefttoprightbottom`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> left,top,bottom,right</span></span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの左端、上端、右端および下端に追加（負の値の場合は削除）するピクセル数(int、int、int、int、int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの左端、上端、右端および下端に追加（負の値の場合は削除）するスペースの量。元のレイヤーrectのサイズ(real、real、real、real)を基準に正規化された値で表します。 </p></td> 
 </tr> 
</table>

`extend=` は、画像が切り抜かれた ** 後(  `crop=`)にレイヤーに適用され、を含むすべてのレイヤー変換が適用さ `rotate=`れます。

拡張領域は`bgColor=`で埋められます。指定しない場合は、透明のままになります。

`extendN=`の引数値は、`rotate=`を含むレイヤー変換後のレイヤーrectのサイズを基準にして正規化されます。

## プロパティ {#section-8fc94de871f841f3bf5e1df135972ca9}

レイヤー属性。 `layer=comp`の場合にレイヤー0に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`（レイヤーの長方形を変更しない場合）。

## 例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**画像を切り抜き、5ピクセル幅の赤い境界線を追加します。**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**画像の幅を200ピクセルに調整し、画像の上の30ピクセルのマージンにタイトルテキストを追加します。**

合成画像の高さは、画像の縦横比によって異なります。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 関連項目 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md),  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b),  [接触チャネル=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)

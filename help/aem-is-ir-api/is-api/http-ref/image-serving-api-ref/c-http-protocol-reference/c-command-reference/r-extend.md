---
description: レイヤーを拡張 レイヤーに余白を追加するか、レイヤーの長方形をトリミングします。
solution: Experience Manager
title: 拡張
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# 拡張{#extend}

レイヤーを拡張 レイヤーに余白を追加するか、レイヤーの長方形をトリミングします。

`extend= *``*, *``*, *``*, *`lefttoprightbottom`*`

`extendN= *``*, *``*, *``*, *`leftNtopNrightNbottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> left,top,bottom,right</span></span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの左、上、右、下の端（整数、整数、整数、整数）に追加（または負の値の場合は削除）するピクセル数です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>レイヤーrectの左端、上端、右端および下端に追加（負の値の場合は削除）するスペースの量。元のレイヤーrectのサイズ(real、real、real、real)に対する正規化量で表されます。 </p></td> 
 </tr> 
</table>

`extend=` は、画像を切り抜いた後( ) ** にレイヤーに適用され、を含むす `crop=`べてのレイヤー変換が適 `rotate=`用された後に適用されます。

拡張領域は`bgColor=`で埋められます。指定しない場合は透明なままになります。

`extendN=`の引数値は、`rotate=`を含むレイヤー変換後のレイヤーの直角のサイズに対して正規化されます。

## プロパティ {#section-8fc94de871f841f3bf5e1df135972ca9}

レイヤー属性。 `layer=comp`の場合はレイヤ0に適用されます。 エフェクトレイヤでは無視されます。

## 初期設定 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`（レイヤーの長方形を変更しない）。

## 例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**画像を切り抜き、幅5ピクセル、赤い境界線を追加します。**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**画像を幅200ピクセルに拡大縮小し、画像の上の30ピクセルの余白にタイトルテキストを追加します。**

合成画像の高さは、画像の縦横比に応じて異なることに注意してください。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 関連項目 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) 、 [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)、 [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)、 [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)、 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)

---
title: extend
description: レイヤーを拡張します。 レイヤーに余白を追加するか、レイヤーの長方形を切り抜きます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---

# extend{#extend}

レイヤーを拡張します。 レイヤーに余白を追加するか、レイヤーの長方形を切り抜きます。

`extend= *`left`*, *`top`*, *`right`*, *`bottom`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 左 <span class="varname">，上，下，右 </span></span> </p></td> 
  <td class="stentry"> <p>レイヤーシートの左端、上端、右端、下端（int、int、int、int）に追加（または負の値の場合は削除）するピクセル数。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>レイヤーレクトの左端、上端、右端、下端に追加（または負の値の場合は削除）するスペースの量。元のレイヤーレクト（実数、実数、実数）に対する正規化された量で表します。 </p></td> 
 </tr> 
</table>

`extend=` がレイヤーに適用され *後* 画像が切り抜かれ（`crop=`）、`rotate=` を含むすべてのレイヤー変換が適用されます。

拡張領域は `bgColor=` で塗りつぶされます。指定しない場合は、透明のままになります。

`extendN=` の引数値は、`rotate=` を含むレイヤー変換が適用された後、レイヤー rect のサイズを基準に正規化されます。

## プロパティ {#section-8fc94de871f841f3bf5e1df135972ca9}

レイヤー属性。 `layer=comp` の場合はレイヤー 0 に適用されます。 エフェクトレイヤーで無視されます。

## 初期設定 {#section-de7473649cb9406b8d99028c74c4b8dc}

レイヤーの長方形を変更しない場合は、`extend=0,0,0,0` をクリックします。

## 例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**画像を切り抜いてから 5 ピクセル幅の赤い境界線を追加する：**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**画像の幅を 200 ピクセルに拡大・縮小し、タイトルテキストを画像の上の 30 ピクセルの余白に追加します。**

合成画像の高さは、画像の縦横比に応じて異なることに注意してください。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 関連項目 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)、[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)、[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)、[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)、[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)

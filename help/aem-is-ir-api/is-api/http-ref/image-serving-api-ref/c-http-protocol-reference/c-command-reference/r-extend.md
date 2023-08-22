---
title: 延長する
description: レイヤを拡張します。 レイヤーに余白を追加するか、レイヤーの長方形をトリミングします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# 延長する{#extend}

レイヤを拡張します。 レイヤーに余白を追加するか、レイヤーの長方形をトリミングします。

`extend= *`left`*, *`top`*, *`右`*, *`bottom`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> left,top,bottom,right</span></span> </p></td> 
  <td class="stentry"> <p>レイヤーの rect の左端、上端、右端および下端に追加（値が負の場合は削除）するピクセル数（整数、整数、整数、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>値が負の場合に、レイヤー rect の左、上、右、下の端に追加（または削除）するスペースの量。元のレイヤー rect(real、real、real、real) のサイズを基準とした正規化された量で表されます。 </p></td> 
 </tr> 
</table>

`extend=` がレイヤーに適用されます。 *次より後* 画像が切り抜かれます ( `crop=`) と、を含むすべてのレイヤー変換 `rotate=`、が適用されている場合にのみ有効です。

拡張領域は `bgColor=`または、指定しなかった場合、透明なままになります。

の引数値 `extendN=` は、レイヤー変換後のレイヤーの直接のサイズを基準にして、 `rotate=` が適用されている。

## プロパティ {#section-8fc94de871f841f3bf5e1df135972ca9}

レイヤー属性。 次の場合にレイヤー 0 に適用 `layer=comp`. 効果画層で無視されます。

## 初期設定 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`（レイヤーの長方形を変更しない場合）。

## 例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**画像を切り抜いてから、幅 5 ピクセルの赤い境界線を追加します。**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**画像を幅 200 ピクセルに拡大縮小し、画像の上の 30 ピクセルの余白にタイトルテキストを追加します。**

合成画像の高さは、画像の縦横比に応じて異なることに注意してください。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 関連項目 {#section-2d9572be32ca4602b60920b3810f3638}

[切り抜き=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)

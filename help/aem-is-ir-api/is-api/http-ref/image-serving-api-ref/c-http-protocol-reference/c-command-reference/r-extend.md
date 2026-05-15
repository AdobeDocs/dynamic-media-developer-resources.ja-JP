---
title: 拡張
description: レイヤーを拡張： レイヤーに余白を追加するか、レイヤーの長方形を切り抜きます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03db6555-6851-49d4-b0de-5570bf56ad76
TQID: 'https://experienceleague.adobe.com/9toLDEF2GoV-F5J-lxjswISzwgooS4FwqeGF4Gav0tc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 1%

---

# 拡張{#extend}

レイヤーを拡張： レイヤーに余白を追加するか、レイヤーの長方形を切り抜きます。

`extend= *`left`*, *`top`*, *`right`*, *`bottom`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">左、上、下、右</span></span> </p></td> 
  <td class="stentry"> <p>レイヤー矩形の左端、上端、右端、下端（int、int、int、int）に追加するピクセル数（または値が負の場合は削除するピクセル数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>レイヤー矩形の左、上、右、下のエッジに追加する（または値が負の場合は削除する）スペースの量。元のレイヤー矩形のサイズ（実数、実数、実数、実数）に対して正規化された量で表されます。 </p></td> 
 </tr> 
</table>

`extend=`がレイヤー&#x200B;*に適用され、*&#x200B;の後に画像が切り抜かれます（`crop=`）。`rotate=`を含むすべてのレイヤー変換が適用されました。

拡張エリアは`bgColor=`で埋められます。指定しない場合は、透明のままです。

`extendN=`の引数の値は、`rotate=`を含む、レイヤー変換後のレイヤー直交のサイズに対して正規化されます。

## プロパティ {#section-8fc94de871f841f3bf5e1df135972ca9}

レイヤー属性。 `layer=comp`の場合、レイヤー0に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`。レイヤーの長方形は変更されません。

## 例 {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**画像を切り抜き、幅5 ピクセルの赤い境界線を追加：**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**画像の幅を200 ピクセルに拡大/縮小し、画像の上の30 ピクセルの余白にタイトルテキストを追加します。**

合成画像の高さは、画像の縦横比によって異なります。

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## 関連項目 {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)、[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)、[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)、[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)、[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)

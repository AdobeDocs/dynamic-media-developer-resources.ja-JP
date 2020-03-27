---
description: 画像の拡大・縮小 最大解像度の画像を基準にして、レイヤーのソース画像を拡大・縮小します。
seo-description: 画像の拡大・縮小 最大解像度の画像を基準にして、レイヤーのソース画像を拡大・縮小します。
seo-title: scale
solution: Experience Manager
title: scale
topic: Scene7 Image Serving - Image Rendering API
uuid: f5540df8-60d9-4efc-99fe-733cdc8268ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scale{#scale}

画像の拡大・縮小 最大解像度の画像を基準にして、レイヤーのソース画像を拡大・縮小します。

`scale= *`因子`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 因子</span> </p> </td> 
  <td class="stentry"> <p>スケール係数（実数、0.0より大きい） </p></td> 
 </tr> 
</table>

No scaling is applied when `scale=1`. *`factor`* 1.0より小さい場合は縮小され、1.0より大きい場合はソース画像が拡大されます。

## プロパティ {#section-3c7eb45527394fe79b1ddba6c1fcca09}

ソース画像/マスク属性。 現在のレイ `size=` ヤーにもが指定されている場合は無視されます。 Overrides `res=`. に対して指定した場合、レイヤ0に適用されま `layer=comp`す。 レイヤーが画像またはマスクに関連付けられていない場合は無視されます。

## 初期設定 {#section-26e64904362342a5a62c5f6598f330c4}

指定しなかった場合、が使 `res=` 用されます。 を指定 `res=` しない場合、画像は拡大・縮小せずに使用されます。

## 関連項目 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)

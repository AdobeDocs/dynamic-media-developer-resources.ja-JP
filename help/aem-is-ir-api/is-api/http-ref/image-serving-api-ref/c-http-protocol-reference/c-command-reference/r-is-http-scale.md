---
description: 画像を拡大・縮小します。 最大解像度の画像を基準にして、レイヤーソース画像を拡大/縮小します。
solution: Experience Manager
title: scale
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 5%

---

# スケール{#scale}

画像を拡大・縮小します。 最大解像度の画像を基準にして、レイヤーソース画像を拡大/縮小します。

`scale= *`因子`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 因子</span> </p> </td> 
  <td class="stentry"> <p>スケール係数（実数、0.0より大きい） </p></td> 
 </tr> 
</table>

`scale=1`の場合、スケーリングは適用されません。 *`factor`* 1.0より小さく、1.0より大きい場合は、ソースイメージが拡大されます。

## プロパティ {#section-3c7eb45527394fe79b1ddba6c1fcca09}

ソースイメージ/マスクのアトリビュート `size=`が現在の画層に対しても指定されている場合は無視されます。 `res=`を上書きします。 `layer=comp`に対して指定した場合、レイヤ0に適用されます。 レイヤーがイメージまたはマスクに関連付けられていない場合は無視されます。

## 初期設定 {#section-26e64904362342a5a62c5f6598f330c4}

指定しなかった場合は、`res=`が使用されます。 `res=`を指定しない場合、画像は拡大・縮小されずに使用されます。

## 関連項目 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) ,  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)

---
title: scale
description: 画像を拡大・縮小します。 最大解像度の画像を基準に、レイヤーソース画像を倍率で拡大/縮小します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

---

# scale{#scale}

画像を拡大・縮小します。 最大解像度の画像を基準に、レイヤーソース画像を倍率で拡大/縮小します。

`scale= *`要因`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 要因</span> </p> </td> 
  <td class="stentry"> <p>スケール係数（実数、0.0 より大きい値） </p></td> 
 </tr> 
</table>

スケーリングは適用されません。 `scale=1`. *`factor`* 1.0 より小さく、1.0 より大きい場合は、ソースイメージが拡大されます。

## プロパティ {#section-3c7eb45527394fe79b1ddba6c1fcca09}

ソース画像/マスクの属性。 次の場合は無視 `size=` は、現在の画層に対しても指定されます。 上書き `res=`. 次の項目を指定した場合、レイヤ 0 に適用されます。 `layer=comp`. レイヤーが画像またはマスクに関連付けられていない場合は無視されます。

## 初期設定 {#section-26e64904362342a5a62c5f6598f330c4}

指定しない場合、 `res=` が使用されます。 次の場合 `res=` が指定されていない場合、画像は拡大・縮小せずに使用されます。

## 関連項目 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)

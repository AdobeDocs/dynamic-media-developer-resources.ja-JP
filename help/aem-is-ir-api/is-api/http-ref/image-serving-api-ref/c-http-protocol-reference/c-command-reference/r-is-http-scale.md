---
title: スケール
description: 画像を拡大/縮小します。 レイヤーのソース画像を、フル解像度の画像に対する係数で拡大縮小します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# スケール{#scale}

画像を拡大/縮小します。 レイヤーのソース画像を、フル解像度の画像に対する係数で拡大縮小します。

`scale= *` 係数 `*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 要素 </span> </p> </td> 
  <td class="stentry"> <p>尺度係数（実数、0.0 より大きい） </p></td> 
 </tr> 
</table>

`scale=1` の場合、拡大縮小は適用されません。 1.0 より小 *`factor`* いダウンスケールと 1.0 より大きい場合は、ソースイメージが拡大されます。

## プロパティ {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Source image/mask 属性。 現在の画層に `size=` も指定されている場合は無視されます。 `res=` を上書きします。 `layer=comp` に指定されている場合は、画層 0 に適用されます。 レイヤーが画像またはマスクに関連付けられていない場合は無視されます。

## 初期設定 {#section-26e64904362342a5a62c5f6598f330c4}

指定しない場合は、`res=` が使用されます。 `res=` が指定されていない場合、画像は拡大縮小なしで使用されます。

## 関連項目 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)

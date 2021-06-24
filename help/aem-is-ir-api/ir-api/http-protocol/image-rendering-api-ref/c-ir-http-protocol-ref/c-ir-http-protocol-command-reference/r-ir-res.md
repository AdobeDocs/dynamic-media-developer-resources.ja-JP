---
description: 材料の解像度 繰り返し可能なテクスチャまたはデカールイメージの解像度を指定します。
solution: Experience Manager
title: res
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: f207355d-5819-47fc-bda5-27a411449569
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# res{#res}

材料の解像度 繰り返し可能なテクスチャまたはデカールイメージの解像度を指定します。

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>解像度マテリアル解像度の単位（通常はピクセル/インチ）（実数） </p> </td> 
 </tr> 
</table>

デカル転写材の場合、`size=`と`res=`の両方が指定されていると、`size=`が優先されます。

## プロパティ {#section-6a458ddc202f46e0b668c9f040a65cef}

マテリアル属性。 べた塗りマテリアルでは無視されます。 テクスチャも使用する場合にのみ、キャビネットと窓の覆いのマテリアルでのみ使用できます。

## 初期設定 {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`マテリアルがカタログエントリに基づいている場合は、それ以外の場合 `attribute::Resolution`(指定されていな `res= is` い場合または0以下の値に設定されている場合)。

## 関連項目 {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[マテリアル解像度](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b)、 [サイズ= ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)、 [カタログ：：解像度](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7)、 [属性：：解像度](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)

---
description: 材料の解像度 繰り返し可能なテクスチャまたはデカールイメージの解像度を指定します。
seo-description: 材料の解像度 繰り返し可能なテクスチャまたはデカールイメージの解像度を指定します。
seo-title: res
solution: Experience Manager
title: res
topic: Scene7 Image Serving - Image Rendering API
uuid: ae755a92-ad06-4cf2-b627-0b8b14e385c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# res{#res}

材料の解像度 繰り返し可能なテクスチャまたはデカールイメージの解像度を指定します。

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>解像度；マテリアルの解像度の単位（通常はピクセル/インチ）（実数） </p> </td> 
 </tr> 
</table>

デカルの材料の場合、との両方が指 `size=` 定されている `size=` 場合は、が `res=` 使用されます。

## プロパティ {#section-6a458ddc202f46e0b668c9f040a65cef}

マテリアル属性。 べた塗りのマテリアルでは無視されます。 テクスチャを使用する場合に限り、キャビネットと窓のカバーマテリアルでのみ使用できます。

## 初期設定 {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`材料がカタログエントリを基にしている場合は、それ以外の場合(指 `attribute::Resolution`定されて `res= is` いない場合、または0以下の値に設定されている場合)。

## 関連項目 {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[マテリアルの解](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b)像度 [、](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)size= [、](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7)catalog::Resolution [、attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)

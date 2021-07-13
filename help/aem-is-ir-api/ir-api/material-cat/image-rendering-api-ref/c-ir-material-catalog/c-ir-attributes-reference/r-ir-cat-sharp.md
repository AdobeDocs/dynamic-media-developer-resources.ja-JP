---
description: デフォルトの材料のシャープニング。 特定のカタログレコードに有効なカタログシャープ値が含まれていない場合に使用する、デフォルトのマテリアルシャープモードを設定します。
solution: Experience Manager
title: 'シャープ '
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 10%

---

# シャープ {#sharp}

デフォルトの材料のシャープニング。 特定のカタログレコードに有効なcatalog::Sharp値が含まれていない場合に使用する、既定のマテリアルシャープモードを設定します。

## プロパティ {#section-dcb810d01b8a40eb991d555a3cbe48b9}

列挙

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>シャープは適用されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>通常のシャープニング（変換後） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>代替シャープニング（変換前）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>よりシャープにする（変換の前と後の両方）。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-613130fca7c04ce7a7734265f27aa1ea}

`default::Sharp`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-7771824f2822443ab0297e8793bb48ae}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) 、 [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)、 [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)

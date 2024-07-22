---
title: シャープ
description: デフォルトのマテリアルシャープ。 特定のカタログレコードに有効なカタログのシャープ値が含まれていない場合に使用する、デフォルトのマテリアルシャープモードを設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 8%

---

# シャープ{#sharp}

デフォルトのマテリアルシャープ。 特定のカタログレコードに有効な `catalog::Sharp` 値が含まれていない場合に使用する、デフォルトのマテリアルシャープニングモードを設定します。

## プロパティ {#section-dcb810d01b8a40eb991d555a3cbe48b9}

列挙値。

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>シャープニングなし。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>（変換後の）通常のシャープ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>（変換前の）代替シャープ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>シャープニングの強化（変換前と変換後の両方） </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-613130fca7c04ce7a7734265f27aa1ea}

定義されていない場合または空の場合は `default::Sharp` から継承します。

## 関連項目 {#section-7771824f2822443ab0297e8793bb48ae}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0)、[sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)、[catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)

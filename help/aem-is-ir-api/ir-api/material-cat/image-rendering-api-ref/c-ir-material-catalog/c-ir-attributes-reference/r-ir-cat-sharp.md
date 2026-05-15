---
title: シャープ
description: デフォルトのマテリアルシャープニング 特定のカタログレコードに有効なカタログシャープ値が含まれていない場合に、デフォルトのマテリアルシャープモードを設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
TQID: 'https://experienceleague.adobe.com/BUhpguI3knVzevI-ymAt4Xz-faYKbXgHMXW0O9Mf8oo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 88
ht-degree: 7%

---

# シャープ{#sharp}

デフォルトのマテリアルシャープニング 特定のカタログレコードに有効な`catalog::Sharp`値が含まれていない場合に備えて、デフォルトのマテリアルシャープニングモードを設定します。

## プロパティ {#section-dcb810d01b8a40eb991d555a3cbe48b9}

列挙：

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>シャープなし。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>通常のシャープ処理（変換後）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>（変形の前に）シャープを切り替えます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>よりシャープにする（トランスフォームの前と後の両方） </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-613130fca7c04ce7a7734265f27aa1ea}

定義されていない場合や空の場合は、`default::Sharp`から継承されます。

## 関連項目 {#section-7771824f2822443ab0297e8793bb48ae}

[ カタログ：：シャープ ](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0)、[ シャープ=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)、[ カタログ：:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)

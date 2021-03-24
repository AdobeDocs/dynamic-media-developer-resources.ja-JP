---
description: 初期設定のマテリアルのシャープ 特定のカタログレコードに有効なカタログシャープ値が含まれていない場合に使用する、初期設定のマテリアルシャープの適用モードを設定します。
solution: Experience Manager
title: 'シャープ '
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 10%

---


# シャープ {#sharp}

初期設定のマテリアルのシャープ 特定のカタログレコードに有効なcatalog::Sharp値が含まれていない場合に使用する、初期設定のマテリアルシャープの適用モードを設定します。

## プロパティ {#section-dcb810d01b8a40eb991d555a3cbe48b9}

列挙。

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>シャープなし </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>通常のシャープ（変換後） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>代替シャープ（変換前） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>よりシャープにする（変換の前と後の両方）。 </p> </td> 
 </tr> 
</table>

## 初期設定 {#section-613130fca7c04ce7a7734265f27aa1ea}

定義されていない場合や空の場合は`default::Sharp`から継承されます。

## 関連項目 {#section-7771824f2822443ab0297e8793bb48ae}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a),  [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)

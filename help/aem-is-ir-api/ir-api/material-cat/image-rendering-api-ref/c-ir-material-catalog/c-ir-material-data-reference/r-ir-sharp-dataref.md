---
description: シャープ. シャープアトリビュート。レンダリング時にマテリアルをシャープにするタイミングを指定します。
solution: Experience Manager
title: シャープ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 9%

---

# シャープ {#sharp}

シャープ. シャープアトリビュート。レンダリング時にマテリアルをシャープにするタイミングを指定します。

シャープの種類と量は、ビネットによって、デフォルトのマテリアルテンプレートを使用するか、を使用して制御されます `catalog::RenderSettings`.

## プロパティ {#section-aac81b1a611b4bca90b8544eae7896df}

列挙。

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>シャープは適用されません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>通常のシャープ（変形後） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>別のシャープ（変形前） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>よりシャープにする（変形前と変形後の両方）。 </p></td> 
 </tr> 
</table>

ソリッドカラーマテリアルでは無視され、その他のすべてのマテリアルではオプションです。

## 初期設定 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` フィールドが存在しない場合、空の場合、または値がサポートされている選択肢の 1 つでない場合に、が使用されます。

## 関連項目 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)

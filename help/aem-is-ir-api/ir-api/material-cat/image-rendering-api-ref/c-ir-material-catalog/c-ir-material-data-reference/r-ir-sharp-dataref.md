---
description: シャープ. シャープアトリビュート：レンダリング中にマテリアルをシャープにするタイミングを指定します。
solution: Experience Manager
title: 'シャープ '
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 10%

---

# シャープ {#sharp}

シャープ. シャープアトリビュート：レンダリング中にマテリアルをシャープにするタイミングを指定します。

シャープの種類と量は、ビネットでデフォルトのマテリアルテンプレートを使用するか、`catalog::RenderSettings`を使用して制御します。

## プロパティ {#section-aac81b1a611b4bca90b8544eae7896df}

列挙

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
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
  <td class="stentry"> <p>よりシャープにする（変換の前と後の両方）。 </p></td> 
 </tr> 
</table>

ソリッドカラーマテリアルでは無視され、その他のマテリアルではオプションです。

## 初期設定 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` は、フィールドが存在しない場合、空の場合、または値がサポートされている選択肢の1つでない場合に使用されます。

## 関連項目 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) 、 [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd)、 [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)

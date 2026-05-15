---
description: シャープ化： シャープ属性は、レンダリング中にマテリアルをシャープ化するタイミングを決定します。
solution: Experience Manager
title: シャープ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
TQID: 'https://experienceleague.adobe.com/e9pUY-R7wpieviEUxzGeuyGduEKTLGf4cZz57Kc2Qhs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 6%

---

# シャープ{#sharp}

シャープ化： シャープ属性は、レンダリング中にマテリアルをシャープ化するタイミングを決定します。

シャープの種類と量は、デフォルトのマテリアルテンプレートまたは`catalog::RenderSettings`を使用して、周辺光量補正によって制御されます。

## プロパティ {#section-aac81b1a611b4bca90b8544eae7896df}

列挙：

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
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
  <td class="stentry"> <p>よりシャープにする（トランスフォームの前と後の両方） </p></td> 
 </tr> 
</table>

単色のマテリアルでは無視され、他のすべてのマテリアルではオプションです。

## 初期設定 {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

フィールドが存在しない場合、フィールドが空の場合、または値がサポートされている選択肢のいずれでもない場合は、`attribute::Sharpening`が使用されます。

## 関連項目 {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[属性：：シャープニング &#x200B;](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297)、[&#x200B; カタログ：:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd)、[&#x200B; シャープ=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)

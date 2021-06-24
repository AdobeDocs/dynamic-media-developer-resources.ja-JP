---
description: デカルの位置 デカル画像のアンカー=点から、対象のビネットオブジェクトで定義されたデカールの原点までのオフセットをインチ単位で定義します。
solution: Experience Manager
title: pos
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 531f1465-2bec-46b6-a41e-54d993cbf410
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 4%

---

# pos{#pos}

デカルの位置 デカル画像のアンカー=点から、対象のビネットオブジェクトで定義されたデカールの原点までのオフセットをインチ単位で定義します。

`pos=x,y`

<table id="simpletable_DB3B64EFB67A47AD843812324ABFAE45"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,<span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）での相対位置の調整（実数、実数）。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-50371cfa4e244bc49d2295a918749258}

マテリアル属性。 デカル以外の材料では無視されます。

## 初期設定 {#section-1b66efab054c45ca8d67d6a9865020f4}

`pos=0,0`. デカル転写のアンカーポイントをビネットオブジェクトのデカールの原点に合わせます。

## 関連項目 {#section-7cd8139481334ed79704d628b5bbd236}

[シーン座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)、 [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

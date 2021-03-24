---
description: デカールの位置 デカールイメージのanchor=点から、ターゲットビネットオブジェクトによって定義されたデカール接触チャネル点までのオフセットをインチ単位で定義します。
solution: Experience Manager
title: pos
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# pos{#pos}

デカールの位置 デカールイメージのanchor=点から、ターゲットビネットオブジェクトによって定義されたデカール接触チャネル点までのオフセットをインチ単位で定義します。

`pos=x,y`

<table id="simpletable_DB3B64EFB67A47AD843812324ABFAE45"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,<span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>シーンの座標単位（通常はインチ）での相対位置の調整（実数、実数） </p></td> 
 </tr> 
</table>

## プロパティ {#section-50371cfa4e244bc49d2295a918749258}

マテリアル属性 デカル以外のマテリアルでは無視されます。

## 初期設定 {#section-1b66efab054c45ca8d67d6a9865020f4}

`pos=0,0`. デカル転写のアンカーポイントをビネットオブジェクトのデカール接触チャネルに合わせます。

## 関連項目 {#section-7cd8139481334ed79704d628b5bbd236}

[シーン座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)、 [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

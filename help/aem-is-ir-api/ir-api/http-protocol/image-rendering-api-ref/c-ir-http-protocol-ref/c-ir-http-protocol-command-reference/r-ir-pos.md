---
title: 位置
description: デカル転写の位置 デカル転写イメージの anchor= ポイントから、ターゲット ビネット オブジェクトで定義されたデカル原点までのオフセットをインチ単位で定義します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 531f1465-2bec-46b6-a41e-54d993cbf410
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 3%

---

# 位置{#pos}

デカル転写の位置 デカル転写イメージの anchor= ポイントから、ターゲット ビネット オブジェクトで定義されたデカル原点までのオフセットをインチ単位で定義します。

`pos=x,y`

<table id="simpletable_DB3B64EFB67A47AD843812324ABFAE45"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,<span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>シーン座標単位（通常はインチ）の相対位置調整（実際、実際）。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-50371cfa4e244bc49d2295a918749258}

マテリアル アトリビュート。 デカール以外のマテリアルでは無視されます。

## 初期設定 {#section-1b66efab054c45ca8d67d6a9865020f4}

`pos=0,0`。 デカル転写のアンカーポイントをビネット オブジェクトのデカル原点に位置合わせします。

## 関連項目 {#section-7cd8139481334ed79704d628b5bbd236}

[&#x200B; シーン座標 &#x200B;](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

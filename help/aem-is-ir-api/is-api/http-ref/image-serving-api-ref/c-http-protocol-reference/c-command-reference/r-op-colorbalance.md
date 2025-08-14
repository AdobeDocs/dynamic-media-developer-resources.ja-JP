---
title: op_colorbalance
description: カラーバランスを調整します。 各RGB カラーコンポーネントの値を個別に調整します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---

# op_colorbalance{#op-colorbalance}

カラーバランスを調整します。 各RGB カラーコンポーネントの値を個別に調整します。

`op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>赤色のコンポーネント調整（–100...+100 int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>緑のコンポーネント調整（–100...+100 int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>青コンポーネント調整（–100...+100 int）。 </p></td> 
 </tr> 
</table>

グレーと CMYK の入力画像データは、ネイティブ変換を使用してRGBに変換されますが、カラーマネジメントが有効な場合は正確ではありません。

## プロパティ {#section-dff9c934f7c1442bbd02379b688d82e2}

[ 画層 ] コマンド： 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。 エフェクトレイヤーで無視されます。 CMYK 画像とレイヤーは、操作が適用される前にRGBに変換されます。

## 初期設定 {#section-08d84ef715964f7daea86f5ef237d199}

色の変化がない `op_colorbalance=0,0,0` 合。

## 例 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

カラーバランスを赤の方に押します。

...`&op_colorBalance=100,0,0&`...

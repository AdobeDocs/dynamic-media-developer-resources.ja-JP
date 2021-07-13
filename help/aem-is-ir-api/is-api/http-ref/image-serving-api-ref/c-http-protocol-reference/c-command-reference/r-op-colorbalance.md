---
description: カラーバランスを調整します。 各RGBカラーコンポーネントの値を個別に調整します。
solution: Experience Manager
title: op_colorbalance
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# op_colorbalance{#op-colorbalance}

カラーバランスを調整します。 各RGBカラーコンポーネントの値を個別に調整します。

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>赤の成分調整(-100...+100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>緑のコンポーネント調整(-100...+100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>青色成分の調整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

グレーおよびCMYK入力画像データは、カラーマネジメントが有効な場合は正確ではないナイーブ変換を使用してRGBに変換されます。

## プロパティ {#section-dff9c934f7c1442bbd02379b688d82e2}

レイヤコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤでは無視されます。 CMYK画像とレイヤーは、操作が適用される前にRGBに変換されます。

## 初期設定 {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` 色は変わらない

## 例 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

カラーバランスを赤に近づけます。

... `&op_colorBalance=100,0,0&`...

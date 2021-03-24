---
description: カラーバランスを調整 各RGBカラーコンポーネントの値を個別に調整します。
solution: Experience Manager
title: op_colorbalance
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---


# op_colorbalance{#op-colorbalance}

カラーバランスを調整 各RGBカラーコンポーネントの値を個別に調整します。

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>赤のコンポーネント調整(-100 ～ 100 int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>緑のコンポーネント調整(-100 ～ 100 int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>青のコンポーネント調整(-100 ～ 100 int) </p></td> 
 </tr> 
</table>

カラーマネジメントが有効な場合、正確でないネイティブ変換を使用して、グレーおよびCMYK入力画像データをRGBに変換します。

## プロパティ {#section-dff9c934f7c1442bbd02379b688d82e2}

レイヤーコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤーでは無視されます。 CMYK画像とレイヤーは、操作の適用前にRGBに変換されます。

## 初期設定 {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` 色は変わらない

## 例 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

カラーバランスを赤に近づけます。

... `&op_colorBalance=100,0,0&`...

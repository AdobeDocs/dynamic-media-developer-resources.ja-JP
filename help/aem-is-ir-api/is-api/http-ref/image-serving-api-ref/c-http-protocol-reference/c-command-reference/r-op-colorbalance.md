---
description: カラーバランスを調整 各RGBカラーコンポーネントの値を個別に調整します。
seo-description: カラーバランスを調整 各RGBカラーコンポーネントの値を個別に調整します。
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
topic: Scene7 Image Serving - Image Rendering API
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '126'
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

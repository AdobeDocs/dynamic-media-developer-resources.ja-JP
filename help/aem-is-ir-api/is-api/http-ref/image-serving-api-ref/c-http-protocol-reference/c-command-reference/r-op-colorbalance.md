---
title: op_colorbalance
description: カラーバランスを調整します。 各RGB カラーコンポーネントの値を個別に調整します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
TQID: 'https://experienceleague.adobe.com/etLnTD-hMe5kOnvak7n47O0XwOWvqtC5av4FkYZpaGI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 1%

---

# op_colorbalance{#op-colorbalance}

カラーバランスを調整します。 各RGB カラーコンポーネントの値を個別に調整します。

`op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>赤いコンポーネント調整（–100...+100 int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>緑のコンポーネント調整（–100...+100 int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>青色のコンポーネント調整（–100...+100 int）。 </p></td> 
 </tr> 
</table>

グレーとCMYKの入力画像データは、カラーマネジメントが有効になっている場合に正確ではないネイティブ変換を使用してRGBに変換されます。

## プロパティ {#section-dff9c934f7c1442bbd02379b688d82e2}

Layer コマンド。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。 エフェクトレイヤーでは無視されます。 CMYK画像とレイヤーは、操作が適用される前にRGBに変換されます。

## 初期設定 {#section-08d84ef715964f7daea86f5ef237d199}

色の変更がない`op_colorbalance=0,0,0`。

## 例 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

カラーバランスを赤に向かってプッシュします。

... `&op_colorBalance=100,0,0&`...

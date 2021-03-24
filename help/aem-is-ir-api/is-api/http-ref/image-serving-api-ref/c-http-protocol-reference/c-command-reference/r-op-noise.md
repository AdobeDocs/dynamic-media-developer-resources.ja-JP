---
description: 追加ノイズ 前景画像データまたはエフェクトレイヤーの前景にランダムなノイズを追加します。
solution: Experience Manager
title: op_noise
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# op_noise{#op-noise}

追加ノイズ 前景画像データまたはエフェクトレイヤーの前景にランダムなノイズを追加します。

`op_noise= *``*[,uniform|gaussian[, *`valmonochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>ノイズの量（パーセント）(0 ～ 100 int) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 一様な</span> </p> </td> 
   <td colname="col2"> <p>「均一ノイズ分布」を選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ガウス</span> </p> </td> 
   <td colname="col2"> <p>ガウスノイズ分布を選択 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monichrome</span> </p> </td> 
   <td colname="col2"> <p>カラーノイズの場合は0に設定し、グレーノイズの場合は1に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* は無視されます。

## プロパティ {#section-1f1a64c791f545a3bf1abd0b0e575d87}

レイヤーコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。

## 初期設定 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`（ノイズなし）。

---
description: 追加ノイズ 前景画像データまたはエフェクトレイヤーの前景にランダムなノイズを追加します。
seo-description: 追加ノイズ 前景画像データまたはエフェクトレイヤーの前景にランダムなノイズを追加します。
seo-title: op_noise
solution: Experience Manager
title: op_noise
topic: Scene7 Image Serving - Image Rendering API
uuid: 531f7a94-149b-4090-a163-a1895156250b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 1%

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

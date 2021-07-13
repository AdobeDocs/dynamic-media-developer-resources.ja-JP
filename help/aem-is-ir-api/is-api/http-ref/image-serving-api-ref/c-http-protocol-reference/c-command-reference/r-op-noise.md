---
description: ノイズを追加します。 前景画像データまたはエフェクトレイヤーの前景にランダムノイズを追加します。
solution: Experience Manager
title: op_noise
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# op_noise{#op-noise}

ノイズを追加します。 前景画像データまたはエフェクトレイヤーの前景にランダムノイズを追加します。

`op_noise= *``*[,uniform|gaussian[, *`valmonochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>ノイズの量（パーセント単位）(0 ～ 100 int)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 均一</span> </p> </td> 
   <td colname="col2"> <p>均一なノイズ分布を選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ガウス</span> </p> </td> 
   <td colname="col2"> <p>ガウスノイズ分布を選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> モノクロ</span> </p> </td> 
   <td colname="col2"> <p>カラーノイズの場合は0に、グレーノイズの場合は1に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* は、グレースケール画像では無視されます。

## プロパティ {#section-1f1a64c791f545a3bf1abd0b0e575d87}

レイヤコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。

## 初期設定 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`（ノイズなし）。

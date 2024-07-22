---
title: op_noise
description: ノイズを追加します。 前景画像データまたはエフェクトレイヤーの前景にランダムノイズを追加します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---

# op_noise{#op-noise}

ノイズを追加します。 前景画像データまたはエフェクトレイヤーの前景にランダムノイズを追加します。

`op_noise= *`val`*[,uniform|gaussian[, *`monochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>ノイズの量（パーセント）（0～100 整数）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>制服 <span class="codeph"> 着 </span> </p> </td> 
   <td colname="col2"> <p>均一なノイズ分布を選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ガウシ <span class="codeph"> ン </span> </p> </td> 
   <td colname="col2"> <p>「ガウス分布」を選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>モノクロ <span class="varname"></span> </p> </td> 
   <td colname="col2"> <p>カラーノイズの場合は 0、グレーノイズの場合は 1 に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

グレースケール画像の場合、*`monochrome`* は無視されます。

## プロパティ {#section-1f1a64c791f545a3bf1abd0b0e575d87}

[ 画層 ] コマンド： 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。

## 初期設定 {#section-d548868fa4b64a60bcb481cad1f8113e}

ノイズ `op_noise=0,uniform,0` ないでください。

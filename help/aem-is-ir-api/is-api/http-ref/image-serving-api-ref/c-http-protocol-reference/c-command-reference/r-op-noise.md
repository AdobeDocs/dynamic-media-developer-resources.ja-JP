---
title: op_noise
description: ノイズを追加します。 前景の画像データまたはエフェクトレイヤーの前景にランダムノイズを追加します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
TQID: 'https://experienceleague.adobe.com/Awfk7mrYylvJeu8mSTa--aSoVMx8Mk6IqDC6ZtFFu4U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 1%

---

# op_noise{#op-noise}

ノイズを追加します。 前景の画像データまたはエフェクトレイヤーの前景にランダムノイズを追加します。

`op_noise= *`val`*[,uniform|gaussian[, *` モノクロ `*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>ノイズの量（パーセント）（0 ～ 100 int）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">均一</span> </p> </td> 
   <td colname="col2"> <p>均一なノイズ分布を選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ガウス </span> </p> </td> 
   <td colname="col2"> <p>ガウス ノイズ分布を選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> モノクロ </span> </p> </td> 
   <td colname="col2"> <p>カラーノイズは0に、グレーノイズは1に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

グレースケール画像では&#x200B;*`monochrome`*&#x200B;は無視されます。

## プロパティ {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Layer コマンド。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。

## 初期設定 {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0` （ノイズなし）。

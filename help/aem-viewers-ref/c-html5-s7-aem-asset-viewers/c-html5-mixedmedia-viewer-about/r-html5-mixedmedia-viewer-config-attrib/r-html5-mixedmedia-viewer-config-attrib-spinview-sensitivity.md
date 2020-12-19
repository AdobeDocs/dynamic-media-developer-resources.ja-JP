---
description: 'null'
seo-description: 'null'
seo-title: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
topic: Dynamic media
uuid: 7c63a7c5-ac75-485d-94ac-d1e133fbe44f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivitySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> マウスのドラッグまたはスワイプで実行される水平スピンと垂直スピンの感度を制御します。 </p> <p> <span class="codeph"> xSensitivity</span> は、マウスを表示の一方の側から他方の側へ水平にドラッグした場合に、水平方向に回転する回数を設定します。例えば、3は、1回のフルドラッグジェスチャで、3回の完了スピンが表示されることを意味します。 </p> <p>同様に、<span class="codeph"> ySensitivity</span>で、垂直方向のスピンの感度を制御します。 値を1に設定した場合、垂直方向の1回のドラッグまたはスワイプによって、表示角度が一番上のスピン平面から一番下（またはその逆）に変わります。 </p> <p><span class="codeph"> ySensitivity</span>に負の値を設定すると、垂直方向のスピンの向きが逆になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`

---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
feature: Dynamic Media Classic，ビューア，SDK/API，スピンセット
role: Developer,Business Practitioner
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensitivitySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span> [,  <span class="varname"> ySensitivity</span> ]</span> </p> </td> 
   <td colname="col2"> <p> マウスのドラッグまたはスワイプで実行される水平および垂直スピンの感度を制御します。 </p> <p> <span class="codeph"> </span> xSensitivityは、ユーザーがマウスをビューの片側から他方に向かって水平にドラッグした場合に、水平方向の製品の回転数を設定します。例えば、3は、1回のフルドラッグジェスチャで、3回の完全スピンが表示されることを意味します。 </p> <p>同様に、<span class="codeph"> ySensitivity</span>は、垂直方向のスピンの感度を制御します。 値が1の場合、垂直方向の1つのドラッグまたはスワイプによって、表示角度が一番上のスピン平面から一番下（またはその逆）に変わります。 </p> <p><span class="codeph"> ySensitivity</span>に負の値を設定すると、垂直方向のスピンが反転します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`

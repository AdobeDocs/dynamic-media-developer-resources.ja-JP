---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`x 感度 `*[, *`y 感度 `*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> x 感度 </span>[, <span class="varname"> y 感度 </span>]</span> </p> </td> 
   <td colname="col2"> <p> マウスのドラッグまたはスワイプによって実行される水平および垂直スピンの感度を制御します。 </p> <p> <span class="codeph"> xSensitivity</span> ビューの片側から反対側にマウスを水平にドラッグした場合に、水平方向に回転する製品の数を設定します。 例えば、3 つとは、1 回の完全なドラッグ ジェスチャーに対して 3 つの完全なスピンが表示されることを意味します。 </p> <p>同様に、<span class="codeph"> ySensitivity</span> は垂直スピンの感度を制御します。 値が 1 の場合は、1 回の垂直ドラッグまたはスワイプによって、ビュー角度が最上部のスピン プレーンから最下部に変更されます（逆の場合も同様）。 </p> <p><span class="codeph"> ySensitivity</span> に負の値を設定すると、垂直スピンの方向が反転します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`

---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensitivity`*[, *`感度`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> 感度</span>]</span> </p> </td> 
   <td colname="col2"> <p> マウスのドラッグまたはスワイプで実行する水平および垂直スピンの感度を制御します。 </p> <p> <span class="codeph"> xSensitivity</span> ユーザがマウスをビューの片側から他方に向かって水平にドラッグした場合に、水平方向の製品回転の数を設定します。 例えば、「3」は、1 回のフルドラッグジェスチャで、3 回の完全スピンが表示されることを意味します。 </p> <p>同様に、 <span class="codeph"> 感度</span> 垂直方向のスピンの感度を制御します。 値を 1 に設定すると、垂直方向の 1 つのドラッグまたはスワイプによって、表示角度が一番上のスピンプレーンから一番下のスピンプレーン（または逆）に変わります。 </p> <p>に負の値を設定する <span class="codeph"> 感度</span> 垂直方向のスピンの方向を反転します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`

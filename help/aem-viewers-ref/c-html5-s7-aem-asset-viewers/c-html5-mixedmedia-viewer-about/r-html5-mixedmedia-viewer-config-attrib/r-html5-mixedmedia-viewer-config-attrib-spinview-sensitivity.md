---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 68df87db-b3c7-4a42-9ab6-742d96261ecd
TQID: 'https://experienceleague.adobe.com/xRqLAbFehJYLGgevPmISxILSWWyedyBSDkbNZTDs808'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensitivity`*[, *`ySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> マウスのドラッグまたはスワイプで実行する水平および垂直スピンの感度を制御します。 </p> <p> <span class="codeph"> xSensitivity</span>は、ユーザーがマウスをビューの一方の側から他方の側に水平にドラッグした場合に、水平方向の製品の完全な回転の回数を設定します。 例えば、3つとは、ユーザーが1回のフルドラッグジェスチャーに対して3回の完全なスピンを見ることを意味します。 </p> <p>同様に、<span class="codeph">感度</span>は垂直方向のスピンの感度を制御します。 値が1の場合は、1回の垂直方向のドラッグまたはスワイプで、最上位のスピンプレーンから最下位（または逆）にビュー角度が変更されます。 </p> <p><span class="codeph">感度</span>に負の値を設定すると、垂直方向のスピンの方向が反転します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`

---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
TQID: 'https://experienceleague.adobe.com/U3RCx6F9hsywdWgtBZukWi6b-Yh5dWzba-2VvxaPMAU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリック/タップをスピンアクションにマッピングするように設定します。 <span class="codeph"> none </span>に設定すると、ダブルクリック/タップのスピンが無効になります。 <span class="codeph"> ズーム </span>に設定されている場合、1回のスピンステップで画像スピンをクリックします。CTRL+クリックで1回のスピンステップをスピンアウトします。 <span class="codeph"> リセット </span>に設定すると、画像を1回クリックするだけで、スピンが最初のスピンレベルにリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のスピン係数が指定された制限を超えている場合はリセットが適用され、それ以外の場合はスピンが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

デスクトップ コンピューターの`reset`、タッチ デバイスの`zoomReset`。

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`

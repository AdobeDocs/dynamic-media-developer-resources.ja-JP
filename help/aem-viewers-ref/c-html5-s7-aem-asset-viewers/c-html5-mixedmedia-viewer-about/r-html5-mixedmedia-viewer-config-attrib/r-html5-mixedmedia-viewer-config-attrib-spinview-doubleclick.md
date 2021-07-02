---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリック/タップとスピン操作のマッピングを設定します。 <span class="codeph"> none </span>に設定すると、ダブルクリック/タップによるスピンが無効になります。 <span class="codeph"> zoom </span>に設定すると、画像をクリックした場合に1回のスピンステップでスピンします。Ctrlキーを押しながらクリックすると、1つのスピンステップがスピンアウトします。 <span class="codeph"> reset </span>に設定すると、画像をシングルクリックした場合に、初期のスピンレベルまでスピンがリセットされます。 <span class="codeph"> zoomReset </span>では、現在のスピン率が指定の限界値以上の場合はリセットが適用され、それ以外の場合はスピンが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` （デスクトップコンピューターの場合） `zoomReset` （タッチデバイスの場合）

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`

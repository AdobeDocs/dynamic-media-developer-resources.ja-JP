---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリック/タップとスピン操作のマッピングを設定します。 を <span class="codeph"> なし </span> ダブルクリック/タップによるスピンを無効にします。 次に設定した場合： <span class="codeph"> ズーム </span>をクリックすると、画像が 1 回のスピンステップでスピンします。Ctrl キーを押しながらクリックすると、1 つのスピンステップをスピンアウトします。 を <span class="codeph"> リセット </span> を指定すると、画像をシングルクリックした場合にスピンが初期のスピンレベルにリセットされます。 の場合 <span class="codeph"> zoomReset </span>、現在のスピン率が指定された制限以上の場合はリセットが適用され、それ以外の場合はスピンが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` デスクトップコンピュータの場合 `zoomReset` （タッチデバイス）。

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`

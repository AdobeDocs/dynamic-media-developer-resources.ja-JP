---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 18c5c21d-af31-4b1c-ab8b-c04d08650123
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップとズーム操作のマッピングを設定します。を <span class="codeph"> なし </span> は、シングルクリック/タップによるズームを無効にします。 次に設定した場合： <span class="codeph"> ズーム </span> 画像をクリックすると、1 段階ズームインします。Ctrl キーを押しながらクリックすると、1 段階だけズームアウトします。 を <span class="codeph"> リセット </span> を指定すると、画像をシングルクリックした場合に、初期のスピンレベルまでズームがリセットされます。 の場合 <span class="codeph"> zoomReset </span>、現在のズーム率が指定の限界値以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` デスクトップコンピュータの場合 `none` （タッチデバイス）。

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`

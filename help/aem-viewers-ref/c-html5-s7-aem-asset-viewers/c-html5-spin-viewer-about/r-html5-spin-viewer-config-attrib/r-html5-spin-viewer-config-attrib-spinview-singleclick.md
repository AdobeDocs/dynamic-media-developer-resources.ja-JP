---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップとズーム操作のマッピングを設定します。を <span class="codeph"> なし </span> は、シングルクリック/タップによるズームを無効にします。 次に設定した場合： <span class="codeph"> スピン </span> 画像をクリックすると、1 段階ズームインします。Ctrl キーを押しながらクリックすると、1 段階だけズームアウトします。 を <span class="codeph"> リセット </span> を指定すると、画像をシングルクリックした場合に、初期のスピンレベルまでズームがリセットされます。 の場合 <span class="codeph"> zoomReset </span>、現在のズーム率が指定の限界値以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

（オプション）

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` デスクトップコンピュータの場合 `none` （タッチデバイス）。

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`

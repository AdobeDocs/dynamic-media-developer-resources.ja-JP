---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップとズーム操作のマッピングを設定します。を <span class="codeph"> なし </span> は、シングルクリック/タップによるズームを無効にします。 次に設定した場合： <span class="codeph"> ズーム </span> 画像をクリックすると、1 段階ズームインします。Ctrl キーを押しながらクリックすると、1 段階だけズームアウトします。 を <span class="codeph"> リセット </span> を指定すると、画像をシングルクリックした場合に、初期のズームレベルまでズームがリセットされます。 の場合 <span class="codeph"> zoomReset </span>、現在のズーム率が指定の限界値以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`zoomReset`  — デスクトップコンピュータの場合 `none` （タッチデバイス）。

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`

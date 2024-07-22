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
ht-degree: 3%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> シングルクリックまたはタップによるズームアクションのマッピングを設定します。 なし <span class="codeph"> 設定すると </span> シングルクリック/タップズームが無効になります。 <span class="codeph"> ズームに設定した場合 </span> 画像をクリックすると、1 回のズームステップでズームします。Ctrl キーを押しながらクリックすると、1 回のズームステップでズームします。 リセット </span> に設定 <span class="codeph"> ると、画像を 1 回クリックするだけで、ズームが初期ズームレベルにリセットされます。 zoomReset </span> では、現在 <span class="codeph"> ズーム率が指定した制限以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`zoomReset` - デスクトップコンピューターの場合。タッチデバイスの場 `none`。

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`

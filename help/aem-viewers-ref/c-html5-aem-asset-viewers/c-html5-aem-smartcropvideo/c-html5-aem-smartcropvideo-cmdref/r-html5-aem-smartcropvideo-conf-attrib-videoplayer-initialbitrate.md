---
title: SmartCropVideoPlayer.initialbitrate
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 4fc4fefa-b094-4e2e-b8ec-a439f8a1a56c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 2%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

ビデオビューアの設定属性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *` 値 `*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>デスクトップでのビデオの初期再生に使用するビデオのビットレートをキロビット/秒または kbps 単位で設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは、ビットレートが次に低いビデオを開始します。 </p> <p>0<span class="codeph"> に設定 </span> ると、ビデオプレーヤーはできるだけ低いビットレートから開始します。 HTML5 HLS ビデオ（Windows 10 では Firefox、Chrome、Internet Explorer 11）をネイティブサポートしていないシステム、および再生モードが自動 <span class="codeph"> 動に設定されている場合にのみ適用 </span> れます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```

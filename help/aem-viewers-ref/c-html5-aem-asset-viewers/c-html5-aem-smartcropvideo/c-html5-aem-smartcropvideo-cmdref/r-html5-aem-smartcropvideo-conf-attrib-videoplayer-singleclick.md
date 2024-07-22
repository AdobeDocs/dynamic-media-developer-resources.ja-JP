---
title: SmartCropVideoPlayer.singleclick
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f48f0866-4eb7-46c5-a7f5-457df7a568e7
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

スマート切り抜きビデオビューアの設定属性。

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> シングルクリックまたはタップして再生/一時停止を切り替えるためのマッピングを設定します。 なし <span class="codeph"> 設定すると </span> シングルクリックまたはタップして再生/一時停止できなくなります。 <span class="codeph"> playPause</span> に設定されている場合、ビデオをクリックすると、ビデオの再生と一時停止が切り替わります。 一部のデバイスでは、ネイティブコントロールを使用できます。 この場合、シングルクリック <span class="codeph"> 動作 </span> 無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```

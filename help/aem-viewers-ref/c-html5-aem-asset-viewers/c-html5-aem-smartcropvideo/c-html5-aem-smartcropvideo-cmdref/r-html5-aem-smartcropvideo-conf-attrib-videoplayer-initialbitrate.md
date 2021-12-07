---
title: SmartCropVideoPlayer.initialbitrate
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

ビデオビューアの設定属性。

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`値`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 値 </span> </p> </td> 
   <td colname="col2"> <p>デスクトップでのビデオの初期再生に使用するビデオビットレート（キロビット/秒または Kbps）を設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは次に低いビットレートのビデオを開始します。 </p> <p>次に設定した場合： <span class="codeph"> 0 </span>に設定すると、可能な限り低いビットレートからビデオプレーヤーが開始します。 HTML5 HLS ビデオ（Windows 10 では Firefox、Chrome、Internet Explorer 11 ブラウザー）をネイティブでサポートしていないシステムで、再生モードがに設定されている場合にのみ適用されます。 <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```

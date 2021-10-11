---
title: Video360Player.initialbitrate
description: ビデオ 360 ビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 7%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

ビデオ 360 ビューアの設定属性。

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> デスクトップでのビデオの初期再生に使用するビデオビットレート（キロビット/秒または Kbps）を設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは次に低いビットレートのビデオで開始します。 </p> <p><span class="codeph"> 0</span> に設定した場合、ビデオプレーヤーは最も低いビットレートから開始します。 </p> <p>HTML5 HLS ビデオをネイティブでサポートしていないシステム（Windows 10 の Firefox、Chrome、Internet Explorer 11 ブラウザーなど）で、再生モードが auto に設定されている場合にのみ適用されます。 </p> </td> 
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

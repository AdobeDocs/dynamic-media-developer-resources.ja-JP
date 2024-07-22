---
title: VideoPlayer.initialbitrate
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

インタラクティブビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *` 値 `*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 値 </span> </p> </td> 
   <td colname="col2"> <p> デスクトップでのビデオの初期再生に使用するビデオのビットレート（キロビット/秒または kbps）を設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは、次にビットレートが低いビデオから開始します。 </p> <p>0</span> に設定 <span class="codeph"> ると、ビデオプレーヤーはできるだけ低いビットレートから開始します。 </p> <p>HTML5 HLS ビデオがネイティブサポートされていないシステム（Windows 10 では Firefox、Chrome、Internet Explorer 11 ブラウザーなど）で、再生モードが自動に設定されている場合にのみ適用されます。 </p> </td> 
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

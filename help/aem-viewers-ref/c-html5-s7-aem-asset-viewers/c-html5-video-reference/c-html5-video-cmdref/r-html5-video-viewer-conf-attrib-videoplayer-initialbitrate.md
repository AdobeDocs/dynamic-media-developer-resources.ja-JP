---
title: VideoPlayer.initialbitrate
description: ビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

ビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *` 値 `*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>デスクトップでのビデオの初期再生に使用するビデオのビットレート（キロビット/秒または kbps）を設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは、ビットレートが次に低いビデオを開始します。 </p> <p>0</span> に設定 <span class="codeph"> ると、ビデオプレーヤーはできるだけ低いビットレートから開始します。 HTML5 HLS ビデオ（Windows 10 では Firefox、Chromeおよび Internet Explorer 11 ブラウザー）をネイティブサポートしていないシステムで、再生モードが「<span class="codeph"> auto </span>」に設定されている場合にのみ適用されます。 </p> </td> 
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

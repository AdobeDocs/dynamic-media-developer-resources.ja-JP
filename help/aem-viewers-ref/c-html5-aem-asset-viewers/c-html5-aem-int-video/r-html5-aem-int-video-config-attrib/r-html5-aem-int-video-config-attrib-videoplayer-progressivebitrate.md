---
title: VideoPlayer.progressivebitrate
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

インタラクティブビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *` 値 `*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 値 </span> </p> </td> 
   <td colname="col2"> <p> 現在のシステムがアダプティブビデオ再生をサポートしていない場合に、アダプティブビデオセットから再生するビデオのビットレートをキロビット/秒（kbps）で指定します。 </p> <p>コンポーネントは、指定された値に最も近い（ただし超過しない） ビットレートでビデオストリームを取得します。 アダプティブビデオセット内のすべてのビデオストリームの画質が指定した値よりも高い場合、ロジックは最低画質のビットレートを選択します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```

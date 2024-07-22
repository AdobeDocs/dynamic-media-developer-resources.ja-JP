---
title: Video360Player.progressivebitrate
description: Video360 ビューアの設定属性
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Video360 ビューアの設定属性

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *` 値 `*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 値 </span> </p> </td> 
   <td colname="col2"> <p> 現在のシステムがアダプティブビデオ再生をサポートしていない場合に、アダプティブビデオセットから再生するビデオのビットレート（キロビット/秒または kbps）を指定します。 </p> <p>コンポーネントは、指定された値に最も近い（ただし超過しない） ビットレートでビデオストリームを取得します。 アダプティブビデオセット内のすべてのビデオストリームの画質が指定した値よりも高い場合、ロジックは最低画質のビットレートを選択します。 </p> </td> 
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

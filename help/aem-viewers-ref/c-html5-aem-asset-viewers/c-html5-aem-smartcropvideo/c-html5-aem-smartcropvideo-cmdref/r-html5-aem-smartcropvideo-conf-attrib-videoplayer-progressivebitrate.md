---
title: SmartCropVideoPlayer.progressivebitrate
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 7f9f1bfe-c68f-4ad4-a4a3-e0a8952e07af
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---

# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

スマート切り抜きビデオビューアの設定属性。

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`値`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 値</span> </p> </td> 
   <td colname="col2"> <p> 現在のシステムがアダプティブビデオ再生をサポートしていない場合に、アダプティブビデオセットから再生するビデオビットレート（1 秒あたりのキロビット数または Kbps）を指定します。 </p> <p>コンポーネントは、指定された値に可能な限り近い（ただし、超過しない）ビットレートでビデオストリームを取得します。 アダプティブビデオセット内のすべてのビデオストリームが指定した値より高い画質の場合、ロジックは最も低い画質のビットレートを選択します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```

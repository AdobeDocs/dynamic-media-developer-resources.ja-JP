---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic media
uuid: 72438e50-29fc-484f-8a3b-be8909e7864f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

インタラクティブビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 現在のシステムがアダプティブビデオの再生をサポートしていない場合に、アダプティブビデオセットから再生するビデオのビットレートをキロビット/秒(kbps)単位で指定します。 </p> <p>コンポーネントは、指定された値に可能な限り近い（ただし超えない）ビットレートでビデオストリームを取得します。 アダプティブビデオセットのすべてのビデオストリームが指定した値より高い画質を持つ場合、最も低い画質を持つビットレートが選択されます。 </p> </td> 
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


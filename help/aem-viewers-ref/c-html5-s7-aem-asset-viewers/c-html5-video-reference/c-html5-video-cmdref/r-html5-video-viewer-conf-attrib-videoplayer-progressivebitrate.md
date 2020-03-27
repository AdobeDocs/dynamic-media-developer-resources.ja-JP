---
description: ビデオビューアの設定属性。
seo-description: ビデオビューアの設定属性。
seo-title: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic media
uuid: 2e911d35-155e-4afa-aede-52e9d00ae211
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

ビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 現在のシステムでアダプティブビデオの再生がサポートされていない場合に、アダプティブビデオセットから再生するビデオのビットレート（キロビット/秒またはkbps）を指定します。 </p> <p>コンポーネントは、指定された値に可能な限り近い（ただし、超えない）ビットレートでビデオストリームを取得します。 アダプティブビデオセット内のすべてのビデオストリームの画質が指定値より高い場合、ロジックは最も低い画質のビットレートを選択します。 </p> </td> 
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


---
description: ビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ
role: Developer,Business Practitioner
exl-id: 7f9f1bfe-c68f-4ad4-a4a3-e0a8952e07af
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

ビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 現在のシステムでアダプティブビデオの再生がサポートされていない場合に、アダプティブビデオセットから再生する必要のあるビデオのビットレート(kbps)を指定します。 </p> <p>コンポーネントは、指定された値に可能な限り近い（ただし超えない）ビットレートでビデオストリームを取得します。 アダプティブビデオセット内のすべてのビデオストリームの画質が指定した値より高い場合、ロジックは最も低い画質のビットレートを選択します。 </p> </td> 
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

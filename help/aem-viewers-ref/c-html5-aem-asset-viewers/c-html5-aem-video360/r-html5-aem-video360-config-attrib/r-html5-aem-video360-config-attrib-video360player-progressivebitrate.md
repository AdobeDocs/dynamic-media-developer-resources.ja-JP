---
description: ビデオ360ビューアの設定属性。
solution: Experience Manager
title: Video360Player.progressivebitrate
feature: Dynamic Media Classic，ビューア，SDK/API,360 VRビデオ
role: Developer,Business Practitioner
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 7%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

ビデオ360ビューアの設定属性。

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

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

---
title: Video360Player.progressivebitrate
description: Video360 Viewerの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
TQID: 'https://experienceleague.adobe.com/Hn-KzfsFcpgPY4V66gMvEZ0avivukDTEzW-ul3uO1Po'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Video360 Viewerの設定属性。

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`値`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">値</span> </p> </td> 
   <td colname="col2"> <p> 現在のシステムでアダプティブビデオの再生がサポートされていない場合に備えて、アダプティブビデオセットから再生するビデオビットレート（キロビット/秒またはkbps）を指定します。 </p> <p>コンポーネントは、指定された値に最も近い（ただし、それを超えない）ビットレートでビデオストリームをピックアップします。 アダプティブビデオセット内のすべてのビデオストリームの画質が指定された値よりも高い場合、ロジックは最も低い画質のビットレートを選択します。 </p> </td> 
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

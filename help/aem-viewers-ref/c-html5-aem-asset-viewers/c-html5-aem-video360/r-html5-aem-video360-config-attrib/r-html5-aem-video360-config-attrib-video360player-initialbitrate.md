---
title: Video360Player.initialbitrate
description: Video360 Viewerの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
TQID: 'https://experienceleague.adobe.com/WQzO6KrubdHhlXoJgOmHxwsGXvSbPSbyJNVo-VnOz0k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 2%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Video360 Viewerの設定属性。

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`値`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">値</span> </p> </td> 
   <td colname="col2"> <p> デスクトップ上のビデオの初期再生に使用されるビデオビットレート（キロビット/秒またはkbps）を設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは、次にビットレートが低いビデオから始まります。 </p> <p><span class="codeph"> 0</span>に設定した場合、ビデオプレーヤーは可能な限り低いビットレートから開始されます。 </p> <p>HTML5 HLS ビデオがネイティブにサポートされていないシステム（Windows 10上のFirefox、Chrome、Internet Explorer 11 ブラウザーなど）、および再生モードが「自動」に設定されている場合にのみ適用されます。 </p> </td> 
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

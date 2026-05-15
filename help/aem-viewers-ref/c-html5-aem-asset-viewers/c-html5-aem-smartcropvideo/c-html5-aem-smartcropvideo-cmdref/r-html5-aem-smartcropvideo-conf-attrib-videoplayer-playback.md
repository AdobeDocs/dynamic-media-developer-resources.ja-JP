---
title: SmartCropVideoPlayer.playback
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6df94fe7-30ea-42f1-a39e-50219259a098
TQID: 'https://experienceleague.adobe.com/IqYyA0CUeENnFYkZ4JLccu--zLHlAOXt7Dhx5gsqZb8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

スマート切り抜きビデオビューアの設定属性。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自動|プログレッシブ </span> </p> </td> 
   <td colname="col2"> <p> ビューアで使用される再生のタイプを設定します。 <span class="codeph">自動</span>が設定されている場合、ほとんどのデスクトップブラウザーとすべてのiOS デバイスで、ビューアはHTML5 ストリーミングビデオをHLS形式で使用します。 これは、古いInternet ExplorerやAndroid™などの特定のシステムでのHTML 5のプログレッシブ再生にフォールバックします。 </p> <p><span class="codeph"> progressive</span>が指定されている場合、ビューアはブラウザーでネイティブにサポートされているHTML 5の再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードとプログレッシブモードでの再生選択について詳しくは、Viewer SDK ユーザーガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

ビューアが外部ビデオを使用する場合は無視されます。 [外部ビデオ サポートを参照してください]
（../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3）。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

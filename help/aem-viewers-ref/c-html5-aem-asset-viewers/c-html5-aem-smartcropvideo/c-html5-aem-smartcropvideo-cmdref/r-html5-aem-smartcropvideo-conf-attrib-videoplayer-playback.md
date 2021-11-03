---
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
title: SmartCropVideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

スマート切り抜きビデオビューアの設定属性。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアで使用する再生の種類を設定します。 条件 <span class="codeph"> auto</span> が設定されている場合、ほとんどのデスクトップブラウザーとすべてのiOSデバイスで、ビューアは HLS 形式のHTML5 ストリーミングビデオを使用します。 古い Internet Explorer や Android などの特定のシステムでは、プログレッシブHTML5 再生にフォールバックされます。 </p> <p>If <span class="codeph"> 進行性</span> を指定した場合、ビューアは、ブラウザーでネイティブにサポートされているHTML5 再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードとプログレッシブモードでの再生の選択について詳しくは、Viewer SDK ユーザガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

ビューアが外部ビデオで動作する場合は無視されます。 詳しくは、 [外部ビデオのサポート]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

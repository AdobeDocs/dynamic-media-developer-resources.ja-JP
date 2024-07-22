---
title: SmartCropVideoPlayer.playback
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6df94fe7-30ea-42f1-a39e-50219259a098
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

スマート切り抜きビデオビューアの設定属性。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアが使用する再生のタイプを設定します。 auto</span><span class="codeph"> 設定すると、ほとんどのデスクトップブラウザーとすべてのiOS デバイスで、ビューアは HLS 形式のHTML5 ストリーミングビデオを使用します。 古い Internet Explorer やAndroid™ などの特定のシステムでは、プログレッシブ HTML5 再生にフォールバックします。 </p> <p>プログレッシブ </span><span class="codeph"> 指定した場合、ビューアは、ブラウザーでネイティブにサポートされているHTML5 での再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動およびプログレッシブモードでの再生の選択について詳しくは、『 Viewer SDK User Guide 』を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

ビューアが外部ビデオを操作する場合は無視されます。 [ 外部ビデオのサポート ] を参照してください。
（../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3）を参照してください。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

---
description: ビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ
role: Developer,Business Practitioner
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

ビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアで使用する再生のタイプを設定します。 <span class="codeph"> auto</span>が設定されている場合、ほとんどのデスクトップブラウザーとすべてのiOSデバイスで、ビューアはHLS形式のHTML5ストリーミングビデオを使用します。 古いInternet ExplorerやAndroidなどの特定のシステムでのプログレッシブHTML5再生にフォールバックされます。 </p> <p><span class="codeph"> progressive</span>を指定した場合、ビューアは、ブラウザーでネイティブサポートされているHTML5再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードとプログレッシブモードでの再生の選択について詳しくは、ビューアSDKユーザガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

ビューアが外部ビデオで動作する場合は無視されます。 [外部ビデオサポート](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)を参照してください。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

---
title: VideoPlayer.playback
description: ビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

ビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアで使用する再生の種類を設定します。 条件 <span class="codeph"> auto</span> が設定されている場合、ほとんどのデスクトップブラウザーとすべてのiOSデバイスで、ビューアは HLS 形式のHTML5 ストリーミングビデオを使用します。 古い Internet Explorer や Android™などの特定のシステムでは、プログレッシブHTML5 再生に戻ります。 </p> <p>If <span class="codeph"> 進行性</span> を指定した場合、ビューアは、ブラウザーでネイティブにサポートされているHTML5 再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードとプログレッシブモードでの再生の選択について詳しくは、ビューア SDK ユーザガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

ビューアが外部ビデオで動作する場合は無視されます。 詳しくは、 [外部ビデオのサポート](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

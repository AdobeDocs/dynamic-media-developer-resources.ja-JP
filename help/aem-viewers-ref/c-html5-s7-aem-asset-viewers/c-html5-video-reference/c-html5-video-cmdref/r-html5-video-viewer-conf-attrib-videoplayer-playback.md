---
description: ビデオビューアの設定属性。
seo-description: ビデオビューアの設定属性。
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 5ab7a322-9de0-4a26-95be-b9b2ff8e5a84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

ビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアが使用する再生のタイプを設定します。 <span class="codeph"> auto</span>が設定されている場合、ほとんどのデスクトップブラウザーとすべてのiOSデバイスでは、ビューアはHLS形式のHTML5ストリーミングビデオを使用します。 古いInternet ExplorerやAndroidなどの特定のシステムでは、プログレッシブHTML5再生にフォールバックされます。 </p> <p><span class="codeph"> progressive</span>を指定した場合、ビューアはブラウザーでネイティブサポートされているHTML5の再生にのみ依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードとプログレッシブモードでの再生の選択について詳しくは、ビューアSDKユーザガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

ビューアが外部ビデオを扱う場合は無視されます。 [外部ビデオのサポート](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)を参照してください。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```


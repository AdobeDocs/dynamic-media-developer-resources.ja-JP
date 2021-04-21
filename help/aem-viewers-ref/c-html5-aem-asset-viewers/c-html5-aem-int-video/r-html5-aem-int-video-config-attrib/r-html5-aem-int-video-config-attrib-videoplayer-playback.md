---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

インタラクティブビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアが使用する再生のタイプを設定します。 </p> <p><span class="codeph"> auto</span>が設定されている場合、ほとんどのデスクトップブラウザーとすべてのiOSデバイスで、ビューアはHLS形式のHTML5ストリーミングビデオを使用し、古いInternet ExplorerやAndroidなどの特定のシステムではプログレッシブHTML5再生にフォールバックします。 </p> <p><span class="codeph"> progressive</span>が設定されている場合、ビューアはブラウザーでネイティブサポートされているHTML5の再生にのみ依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p><span class="codeph"> auto</span>ネイティブモードと<span class="codeph"> progressive</span>ネイティブモードでの再生の選択について詳しくは、HTML5ビューアSDKユーザーガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`

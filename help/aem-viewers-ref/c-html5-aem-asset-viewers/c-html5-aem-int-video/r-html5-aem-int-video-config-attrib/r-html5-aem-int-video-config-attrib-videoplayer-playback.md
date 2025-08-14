---
title: VideoPlayer.playback
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

インタラクティブビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアが使用する再生のタイプを設定します。 </p> <p><span class="codeph"> auto</span> が設定されていると、ほとんどのデスクトップブラウザーとすべてのiOS デバイスで、ビューアはHLS形式のHTML5 ストリーミングビデオを使用します。 また、古い Internet Explorer やAndroid™ などの特定のシステムでは、HTML5 のプログレッシブ再生にフォールバックします。 </p> <p><span class="codeph"> プログレッシブ </span> が設定されている場合、ビューアは、ブラウザーでネイティブにサポートされているHTML5 の再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードおよび <span class="codeph"> プログレッシブ </span> ネイティブモードでの再生 <span class="codeph"> 選択範囲について詳しくは </span> HTML5 ビューアのSDK ユーザーガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`

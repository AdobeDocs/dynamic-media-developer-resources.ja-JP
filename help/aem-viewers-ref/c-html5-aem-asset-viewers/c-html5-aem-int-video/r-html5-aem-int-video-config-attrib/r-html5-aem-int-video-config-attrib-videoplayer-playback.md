---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 2576f433-b9c2-4da1-9a51-f66b71d5df99
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.playback{#videoplayer-playback}

インタラクティブビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアで使用される再生のタイプを設定します。 </p> <p>autoを設定 <span class="codeph"> すると</span> 、ほとんどのデスクトップブラウザとすべてのiOSデバイスで、ビューアはHLS形式のHTML5ストリーミングビデオを使用し、古いInternet ExplorerやAndroidなどの特定のシステムでのプログレッシブHTML5再生にフォールバックします。 </p> <p>プログレッ <span class="codeph"> シブ</span> が設定されている場合、ビューアはブラウザーでネイティブにサポートされているHTML5再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動ネイティブモードとプログレッシブネイティブモードでの再 <span class="codeph"> 生の選択につ</span> いて詳しくは <span class="codeph"></span> 、『HTML5ビューアSDKユーザガイド』を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`

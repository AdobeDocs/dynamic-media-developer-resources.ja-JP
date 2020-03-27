---
description: ビデオ360ビューアの設定属性。
seo-description: ビデオ360ビューアの設定属性。
seo-title: Video360Player.playback
solution: Experience Manager
title: Video360Player.playback
topic: Dynamic media
uuid: ce814963-5cb8-408e-9d57-e7b7e61e0fab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.playback{#video-player-playback}

ビデオ360ビューアの設定属性。

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアで使用される再生のタイプを設定します。 </p> <p>autoを設定 <span class="codeph"> すると</span> 、ほとんどのデスクトップブラウザとすべてのiOSデバイスで、ビューアはHLS形式のHTML5ストリーミングビデオを使用し、古いInternet ExplorerやAndroidなどの特定のシステムでのプログレッシブHTML5再生にフォールバックします。 </p> <p>プログレッ <span class="codeph"> シブ</span> が設定されている場合、ビューアはブラウザーでネイティブにサポートされているHTML5再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動ネイティブモードとプログレッシブネイティブモードでの再 <span class="codeph"> 生の選択につ</span> いて詳しくは <span class="codeph"></span> 、『HTML5ビューアSDKユーザガイド』を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）ビューアが外部ビデオで動作する場合は無視されます。

詳しくは、 [外部ビデオのサポート](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) （英語）を参照してください。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`

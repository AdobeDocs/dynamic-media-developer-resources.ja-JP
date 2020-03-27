---
description: 混在メディアビデオビューアの設定属性。
seo-description: 混在メディアビデオビューアの設定属性。
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic media
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.playback{#videoplayer-playback}

混在メディアビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアで使用される再生のタイプを設定します。 autoを設 <span class="codeph"> 定す</span> ると、ほとんどのデスクトップブラウザとすべてのiOSデバイスで、ビューアはHLS形式のHTML5ストリーミングビデオを使用します。 古いInternet ExplorerやAndroidなどの特定のシステムでのプログレッシブHTML5再生にフォールバックします。 </p> <p>progressiveを指 <span class="codeph"> 定した場合</span> 、ビューアはブラウザーでネイティブにサポートされているHTML5再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードとプログレッシブモードでの再生の選択について詳しくは、ビューアSDKユーザガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`

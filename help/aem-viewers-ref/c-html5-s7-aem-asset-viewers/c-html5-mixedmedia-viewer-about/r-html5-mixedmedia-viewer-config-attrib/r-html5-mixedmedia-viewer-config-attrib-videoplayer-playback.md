---
description: 混在メディアビデオビューアの設定属性。
seo-description: 混在メディアビデオビューアの設定属性。
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
feature: Dynamic Mediaクラシック，ビューア，SDK/API，混在メディアセット
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

混在メディアビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアが使用する再生のタイプを設定します。 <span class="codeph"> auto</span>が設定されている場合、ほとんどのデスクトップブラウザーとすべてのiOSデバイスでは、ビューアはHLS形式のHTML5ストリーミングビデオを使用します。 古いInternet ExplorerやAndroidなどの特定のシステムでは、プログレッシブHTML5再生にフォールバックされます。 </p> <p><span class="codeph"> progressive</span>を指定した場合、ビューアはブラウザーでネイティブサポートされているHTML5の再生にのみ依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードとプログレッシブモードでの再生の選択について詳しくは、ビューアSDKユーザガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`

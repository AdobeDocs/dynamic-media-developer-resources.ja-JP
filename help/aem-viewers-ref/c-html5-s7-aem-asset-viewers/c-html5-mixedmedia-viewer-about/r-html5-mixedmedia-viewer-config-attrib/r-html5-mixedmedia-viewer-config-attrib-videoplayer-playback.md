---
title: VideoPlayer.playback
description: 混在メディアビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# VideoPlayer.playback{#videoplayer-playback}

混在メディアビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアで使用する再生の種類を設定します。 条件 <span class="codeph"> auto</span> が設定されている場合、ほとんどのデスクトップブラウザーとすべてのiOSデバイスで、ビューアは HLS 形式のHTML5 ストリーミングビデオを使用します。 古い Internet Explorer や Android™などの特定のシステムでは、プログレッシブHTML5 再生に戻ります。 </p> <p>If <span class="codeph"> 進行性</span> を指定した場合、ビューアは、ブラウザーでネイティブにサポートされているHTML5 再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードとプログレッシブモードでの再生の選択について詳しくは、ビューア SDK ユーザガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`

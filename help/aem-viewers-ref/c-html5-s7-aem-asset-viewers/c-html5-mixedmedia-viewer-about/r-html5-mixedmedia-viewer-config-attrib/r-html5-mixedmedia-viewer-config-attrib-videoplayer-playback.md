---
title: VideoPlayer.playback
description: 混在メディアビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
TQID: 'https://experienceleague.adobe.com/BWApI4QtEvmeQk1vNJDLtKIvrG3uO02oUlOVEGhyl2s'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

混在メディアビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自動|プログレッシブ </span> </p> </td> 
   <td colname="col2"> <p> ビューアで使用される再生のタイプを設定します。 <span class="codeph">自動</span>が設定されている場合、ほとんどのデスクトップブラウザーとすべてのiOS デバイスで、ビューアはHTML5 ストリーミングビデオをHLS形式で使用します。 これは、古いInternet ExplorerやAndroid™などの特定のシステムでのHTML 5のプログレッシブ再生にフォールバックします。 </p> <p><span class="codeph"> progressive</span>が指定されている場合、ビューアはブラウザーでネイティブにサポートされているHTML 5の再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードとプログレッシブモードでの再生選択について詳しくは、Viewer SDK ユーザーガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`

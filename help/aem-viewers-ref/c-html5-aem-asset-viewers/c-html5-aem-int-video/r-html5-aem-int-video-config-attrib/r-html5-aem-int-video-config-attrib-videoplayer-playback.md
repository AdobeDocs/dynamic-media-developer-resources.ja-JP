---
title: VideoPlayer.playback
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
TQID: 'https://experienceleague.adobe.com/VnLfO1MI9EIpeoP4fpwMufyy-J2g615LOosZ4hLZlt8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

インタラクティブビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自動|プログレッシブ </span> </p> </td> 
   <td colname="col2"> <p> ビューアで使用される再生のタイプを設定します。 </p> <p><span class="codeph">自動</span>が設定されている場合、ほとんどのデスクトップブラウザーとすべてのiOS デバイスで、ビューアはHTML5 ストリーミングビデオをHLS形式で使用します。 また、古いInternet ExplorerやAndroid™などの特定のシステムでは、HTML 5のプログレッシブ再生に戻されます。 </p> <p><span class="codeph"> プログレッシブ </span>が設定されている場合、ビューアはブラウザーでネイティブにサポートされているHTML 5の再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p><span class="codeph"> auto</span>および<span class="codeph"> progressive</span> ネイティブモードでの再生選択について詳しくは、HTML5 ビューア SDK ユーザーガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`

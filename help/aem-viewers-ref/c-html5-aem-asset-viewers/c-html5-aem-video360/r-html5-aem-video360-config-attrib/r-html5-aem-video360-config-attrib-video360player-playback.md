---
title: Video360Player.playback
description: Video360 ビューアの設定属性
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 1%

---

# Video360Player.playback{#video-player-playback}

Video360 ビューアの設定属性

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> ビューアが使用する再生のタイプを設定します。 </p> <p><span class="codeph"> auto</span> が設定されていると、ほとんどのデスクトップブラウザーとすべてのiOS デバイスで、ビューアは HLS 形式のHTML5 ストリーミングビデオを使用します。 また、古い Internet Explorer やAndroid™ などの特定のシステムでは、プログレッシブ HTML5 再生にフォールバックします。 </p> <p><span class="codeph"> プログレッシブ </span> が設定されている場合、ビューアは、ブラウザーでネイティブにサポートされているHTML5 での再生のみに依存し、すべてのシステムでビデオをプログレッシブに再生します。 </p> <p>自動モードと <span class="codeph"> プログレッシブ </span> ネイティブモードでの再生 <span class="codeph"> 選択範囲について詳しくは </span>HTML5 ビューア SDK ユーザーガイドを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。 ビューアが外部ビデオを操作する場合は無視されます。

詳しくは、[ 外部ビデオのサポート ](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) を参照してください。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`

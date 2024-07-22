---
title: VideoPlayer.singleclick
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

インタラクティブビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> シングルクリックまたはタップして再生/一時停止を切り替えるためのマッピングを設定します。 なし <span class="codeph"> 設定すると </span> シングルクリックまたはタップして再生/一時停止できなくなります。 <span class="codeph"> playPause</span> に設定した場合、ビデオを選択するとビデオの再生と一時停止が切り替わります。 一部のデバイスでは、ネイティブコントロールを使用できます。 この場合、<span class="codeph"> しいシングルクリック </span> 動作は無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```

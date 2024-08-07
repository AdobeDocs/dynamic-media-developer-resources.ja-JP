---
title: Video360Player.singleclick
description: Video360 ビューアの設定属性
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# Video360Player.singleclick{#video-player-singleclick}

Video360 ビューアの設定属性

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

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

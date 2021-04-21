---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

インタラクティブビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 再生/一時停止を切り替えるためのシングルクリック/タップのマッピングを設定します。 <span class="codeph"> none</span>に設定すると、シングルクリック/タップで再生/一時停止が無効になります。 <span class="codeph"> playPause</span>に設定すると、ビデオをクリックしたときに、ビデオの再生と一時停止が切り替わります。 一部のデバイスでは、ネイティブのコントロールを使用できます。 この場合、<span class="codeph"> singleclick </span>の動作は無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`playPause`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```

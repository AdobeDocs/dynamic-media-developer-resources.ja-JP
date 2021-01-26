---
description: ビデオ360ビューアの設定属性。
seo-description: ビデオ360ビューアの設定属性。
seo-title: Video360Player.singleclick
solution: Experience Manager
title: Video360Player.singleclick
topic: Dynamic Media
uuid: 2972405c-5c89-45d0-a542-19c7463901b4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 12%

---


# Video360Player.singleclick{#video-player-singleclick}

ビデオ360ビューアの設定属性。

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

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


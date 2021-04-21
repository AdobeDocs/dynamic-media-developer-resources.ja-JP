---
description: ビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

ビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 再生/一時停止を切り替えるためのシングルクリック/タップのマッピングを設定します。 <span class="codeph"> none</span>に設定すると、シングルクリック/タップで再生/一時停止が無効になります。 <span class="codeph"> playPause</span>に設定すると、ビデオをクリックしたときに、ビデオの再生と一時停止が切り替わります。 一部のデバイスでは、ネイティブのコントロールを使用できます。 この場合、<span class="codeph"> singleclick </span>の動作は無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```


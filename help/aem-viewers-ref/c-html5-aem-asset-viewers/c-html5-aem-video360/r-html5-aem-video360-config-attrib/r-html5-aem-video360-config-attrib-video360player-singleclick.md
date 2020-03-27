---
description: ビデオ360ビューアの設定属性。
seo-description: ビデオ360ビューアの設定属性。
seo-title: Video360Player.singleclick
solution: Experience Manager
title: Video360Player.singleclick
topic: Dynamic media
uuid: 2972405c-5c89-45d0-a542-19c7463901b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.singleclick{#video-player-singleclick}

ビデオ360ビューアの設定属性。

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 再生/一時停止を切り替えるためのシングルクリック/タップのマッピングを設定します。 noneを指定する <span class="codeph"> と</span> 、シングルクリック/タップで再生/一時停止が無効になります。 playPauseに設定した場合 <span class="codeph"></span> 、ビデオをクリックすると、ビデオの再生と一時停止が切り替わります。 一部のデバイスでは、ネイティブコントロールを使用できます。 この場合、singleclick動作は <span class="codeph"> 無効</span> です。 </p> </td> 
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


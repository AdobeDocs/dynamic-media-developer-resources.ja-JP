---
description: ビデオ360ビューアの設定属性。
solution: Experience Manager
title: Video360Player.singleclick
feature: Dynamic Media Classic，ビューア，SDK/API,360 VRビデオ
role: Developer,User
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---

# Video360Player.singleclick{#video-player-singleclick}

ビデオ360ビューアの設定属性。

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> 再生/一時停止を切り替えるためのシングルクリック/タップのマッピングを設定します。 <span class="codeph"> none</span>に設定すると、シングルクリック/タップによる再生/一時停止が無効になります。 <span class="codeph"> playPause</span>に設定した場合、ビデオをクリックすると、ビデオの再生と一時停止が切り替わります。 一部のデバイスでは、ネイティブのコントロールを使用できます。 この場合、 <span class="codeph"> singleclick</span>の動作は無効になります。 </p> </td> 
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

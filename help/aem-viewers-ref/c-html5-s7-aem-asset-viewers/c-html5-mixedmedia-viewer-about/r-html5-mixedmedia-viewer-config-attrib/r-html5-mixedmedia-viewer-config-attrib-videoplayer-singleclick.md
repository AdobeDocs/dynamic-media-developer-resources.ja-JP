---
description: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Mediaクラシック，ビューア，SDK/API，混在メディアセット
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 5%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_53A26E1617CB411B9586203CB9AA1AB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> 再生/一時停止を切り替えるためのシングルクリック/タップのマッピングを設定します。 <span class="codeph"> none</span>に設定すると、シングルクリック/タップで再生/一時停止が無効になります。 <span class="codeph"> playPause</span>に設定すると、ビデオをクリックしたときに、ビデオの再生と一時停止が切り替わります。 一部のデバイスでは、ネイティブのコントロールを使用できます。 この場合、<span class="codeph"> singleclick </span>の動作は無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`playPause`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=none`

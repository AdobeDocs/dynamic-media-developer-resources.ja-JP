---
title: SmartCropVideoPlayer.preload
description: ビューアがビデオコンテンツの読み込みを開始する前に開始するかどうかを示します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

ビューアがビデオコンテンツの読み込みを開始する前に開始するかどうかを示します。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> に設定した場合 <span class="codeph"> 1 </span> アセットが設定された直後にビデオのダウンロードが開始される。それ以外の場合は、エンドユーザーまたは API 呼び出しによって再生が開始された後にのみ、プリロードが開始されます。 </p> <p>に設定した場合 <span class="codeph"> 0 </span> 特定の機能は、再び再び再生が始まるまでは機能しない場合があります。特に、シーク操作では、ビデオフレームは更新されません。 ポスター画像が無効になっている場合、ビューアには、最初のビデオフレームではなく空の領域として表示されます。 </p> <p>Internet Explorer 11 および Edge ブラウザーの特定のバージョンでは、ビデオのプリロードの無効化が無視される場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

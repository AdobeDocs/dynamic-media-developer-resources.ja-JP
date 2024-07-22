---
title: SmartCropVideoPlayer.preload
description: 再生が開始される前に、ビューアがビデオコンテンツの読み込みを開始するかどうかを示します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7a83a02e-7b75-4f15-b8c1-aa7b64e6d3bd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

再生が開始される前に、ビューアがビデオコンテンツの読み込みを開始するかどうかを示します。

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"></span> 1 に設定すると、アセットを設定した直後にビデオのダウンロードが開始されます。設定しない場合は、エンドユーザーまたは API 呼び出しによって再生が開始された後でのみ、プリロードが開始されます。 </p> <p><span class="codeph"> 0 に設定すると </span> 再生が再開されるまで、特定の機能が機能しない場合があります。具体的には、シーク操作によってビデオフレームが更新されることはありません。 ポスター画像が無効になっている場合、ビューアには、最初のビデオフレームではなく空の領域が表示されます。 </p> <p>Internet Explorer 11 およびEdgeの特定のバージョンでは、ビデオのプリロードの無効化は無視される場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

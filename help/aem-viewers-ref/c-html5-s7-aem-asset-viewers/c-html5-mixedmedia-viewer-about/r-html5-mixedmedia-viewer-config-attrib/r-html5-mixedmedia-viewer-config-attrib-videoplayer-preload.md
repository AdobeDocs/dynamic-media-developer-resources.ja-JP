---
title: VideoPlayer.preload
description: ビューアがビデオコンテンツの読み込みを開始する前に開始するかどうかを示します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 90fb988a-255c-46fe-b05a-39c95ae8b95d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---

# VideoPlayer.preload{#videoplayer-preload}

ビューアがビデオコンテンツの読み込みを開始する前に開始するかどうかを示します。

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 次に設定した場合： <span class="codeph"> 1 </span> アセットが設定された直後にビデオのダウンロードが開始される。それ以外の場合は、エンドユーザーまたは API 呼び出しによって再生が開始された後にのみ、プリロードが開始されます。 </p> <p>次に設定した場合： <span class="codeph"> 0 </span> 特定の機能は、再生が開始するまで機能しない場合があります。特に、シーク操作では、ビデオフレームは更新されません。 ポスター画像が無効になっている場合、ビューアには、最初のビデオフレームではなく空の領域として表示されます。 </p> <p>Internet Explorer 11 および Edge ブラウザーの特定のバージョンでは、ビデオのプリロードの無効化が無視される場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

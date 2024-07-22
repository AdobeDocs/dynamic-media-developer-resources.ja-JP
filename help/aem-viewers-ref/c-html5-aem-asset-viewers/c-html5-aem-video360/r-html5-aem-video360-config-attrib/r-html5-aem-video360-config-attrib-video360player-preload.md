---
title: Video360Player.preload
description: 再生が開始される前に、ビューアがビデオコンテンツの読み込みを開始するかどうかを示します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# Video360Player.preload{#video-player-preload}

再生が開始される前に、ビューアがビデオコンテンツの読み込みを開始するかどうかを示します。

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">1</span> に設定すると、アセットの設定直後にビデオのダウンロードが開始されます。 そうでない場合、プリロードは、エンドユーザーまたは API 呼び出しによって再生が開始された後でのみ開始されます。 </p> <p><span class="codeph"> 0 </span> に設定すると、再生が開始されるまで特定の機能が機能しない場合があります。 具体的には、シーク操作ではビデオフレームは更新されない。 ポスター画像が無効になっている場合、ビューアには、最初のビデオフレームではなく空の領域が表示されます。 </p> <p>Internet Explorer 11 およびEdgeの特定のバージョンでは、ビデオのプリロードの無効化は無視される場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

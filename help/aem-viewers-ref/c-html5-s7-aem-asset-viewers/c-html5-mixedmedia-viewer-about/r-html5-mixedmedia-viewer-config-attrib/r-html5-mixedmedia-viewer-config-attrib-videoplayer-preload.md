---
description: ビューアがビデオコンテンツの読み込みを開始してから再生を開始するかどうかを示します。
solution: Experience Manager
title: VideoPlayer.preload
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: 90fb988a-255c-46fe-b05a-39c95ae8b95d
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# VideoPlayer.preload{#videoplayer-preload}

ビューアがビデオコンテンツの読み込みを開始してから再生を開始するかどうかを示します。

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 1 </span>に設定すると、アセットの設定直後にビデオのダウンロードが開始されます。それ以外の場合は、エンドユーザーまたはAPI呼び出しによって再生が開始された後にのみ、プリロードが開始されます。 </p> <p><span class="codeph"> 0 </span>に設定すると、特定の機能は再生が開始するまで機能しない場合があります。特に、シーク操作はビデオフレームを更新しません。 ポスター画像が無効になっている場合、ビューアは最初のビデオフレームではなく空の領域として表示されます。 </p> <p>Internet Explorer 11およびEdgeブラウザーの特定のバージョンでは、ビデオのプリロードの無効化は無視される場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

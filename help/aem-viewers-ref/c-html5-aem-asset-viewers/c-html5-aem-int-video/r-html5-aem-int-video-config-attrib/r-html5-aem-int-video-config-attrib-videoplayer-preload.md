---
description: ビューアが再生開始前にビデオコンテンツの読み込みを開始するかどうかを示します。
seo-description: ビューアが再生開始前にビデオコンテンツの読み込みを開始するかどうかを示します。
seo-title: VideoPlayer.preload
solution: Experience Manager
title: VideoPlayer.preload
topic: Dynamic media
uuid: d080465d-7349-4671-aaa4-c49e549d1f64
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.preload{#videoplayer-preload}

ビューアが再生開始前にビデオコンテンツの読み込みを開始するかどうかを示します。

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 1に設定した場合、ア <span class="codeph"> セット </span> の設定直後にビデオのダウンロードが開始されます。それ以外の場合、プリロードは、エンドユーザーまたはAPI呼び出しによって再生が開始された後でのみ開始されます。 </p> <p>0に設定すると、再生が開 <span class="codeph"> 始され </span> るまで特定の機能が動作しない場合があります。具体的には、シーク操作ではビデオフレームは更新されません。 ポスター画像を無効にすると、ビューアは最初のビデオフレームではなく空の領域として表示されます。 </p> <p>ビデオのプリロードを無効にすると、Internet Explorer 11およびEdgeブラウザーの特定のバージョンでは無視される場合があることに注意してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

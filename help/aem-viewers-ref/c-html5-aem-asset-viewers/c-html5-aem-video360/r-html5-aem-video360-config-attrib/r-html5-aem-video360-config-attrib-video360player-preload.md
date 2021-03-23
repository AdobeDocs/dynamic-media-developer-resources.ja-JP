---
description: ビューアが再生開始の前にビデオコンテンツの読み込みを開始するかどうかを示します。
seo-description: ビューアが再生開始の前にビデオコンテンツの読み込みを開始するかどうかを示します。
seo-title: Video360Player.preload
solution: Experience Manager
title: Video360Player.preload
uuid: 6e3b95b8-d585-4164-8665-6211000689fe
feature: Dynamic Mediaクラシック，ビューア，SDK/API,360 VRビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---


# Video360Player.preload{#video-player-preload}

ビューアが再生開始の前にビデオコンテンツの読み込みを開始するかどうかを示します。

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 1 </span>に設定すると、アセットの設定直後にビデオのダウンロードが開始されます。それ以外の場合は、エンドユーザーまたはAPI呼び出しによって再生が開始された後にのみ、開始をプリロードします。 </p> <p><span class="codeph"> 0 </span>に設定した場合、特定の機能は再生開始まで動作しない可能性があります。特に、シーク操作ではビデオフレームは更新されません。 ポスター画像を無効にすると、ビューアは、最初のビデオフレームではなく空の領域として表示されます。 </p> <p>ビデオの事前読み込みを無効にすると、Internet Explorer 11およびEdgeブラウザーの特定のバージョンでは無視される場合があることに注意してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

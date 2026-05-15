---
title: VideoPlayer.preload
description: 再生が開始する前に、ビューアがビデオコンテンツの読み込みを開始するかどうかを示します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 90fb988a-255c-46fe-b05a-39c95ae8b95d
TQID: 'https://experienceleague.adobe.com/6GudMzjM8fboYjgyb-A1HLl6TYirlrQOSjJjt5XWfnw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# VideoPlayer.preload{#videoplayer-preload}

再生が開始する前に、ビューアがビデオコンテンツの読み込みを開始するかどうかを示します。

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 1 </span>に設定されている場合、アセットが設定された直後にビデオのダウンロードが開始されます。それ以外の場合は、エンドユーザーまたはAPI呼び出しによって再生が開始された後にのみプリロードが開始されます。 </p> <p><span class="codeph"> 0 </span>に設定した場合、再生が開始されるまで特定の機能が機能しない可能性があります。具体的には、シーク操作でビデオフレームが更新されません。 ポスター画像が無効になっている場合、ビューアは最初のビデオフレームではなく空の領域として表示されます。 </p> <p>Internet Explorer 11およびEdgeの一部のバージョンでは、ビデオプリロードを無効にできない場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

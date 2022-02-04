---
title: VideoPlayer.mutevolume
description: 混在メディアビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 13398ac5-7137-4345-88b8-5e4df09edb7b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 8%

---

# VideoPlayer.mutevolume{#videoplayer-mutevolume}

混在メディアビデオビューアの設定属性。

`[VideoPlayer.|<containerId>_videoPlayer.]mutevolume=0|1`

<table id="table_2A4F898BBF88417DB0834B7F78637F5D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 初回読み込み時のビデオ再生のミュートモードを設定します。 次に設定した場合： <span class="codeph"> 1 </span> ボリュームはミュートされます。それ以外の場合は、ビデオはサウンドと共に再生されます。 特定のデバイスでは、読み込み時にビデオの再生をミュートすると、ビデオが自動再生される場合もあります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`mutevolume=1`

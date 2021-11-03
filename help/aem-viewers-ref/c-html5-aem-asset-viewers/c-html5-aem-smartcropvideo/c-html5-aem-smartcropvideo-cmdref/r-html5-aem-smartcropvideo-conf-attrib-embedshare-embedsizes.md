---
title: EmbedShare.embedsizes
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: cf075711-1275-4eb2-8cb6-fb2609711c7a
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 11%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

スマート切り抜きビデオビューアの設定属性。

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`幅`*, *`高さ`*[,0|1][; *`幅`*, *`高さ`*[,0|1]]`

埋め込み共有モーダルダイアログボックスのサイズコンボボックスの埋め込みサイズのリストを指定します。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> 埋め込みの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>埋め込みの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> コンボボックスでこのリスト項目を最初に事前に選択する必要があるかどうかを指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```

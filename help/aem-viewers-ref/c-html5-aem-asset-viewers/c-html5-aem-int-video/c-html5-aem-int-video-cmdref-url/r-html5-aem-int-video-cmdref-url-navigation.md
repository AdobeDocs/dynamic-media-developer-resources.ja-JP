---
title: ナビゲーション
description: インタラクティブビデオビューア用のURLコマンド。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9852e723-fd1f-4ade-921b-cfb92bf9f2ad
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 14%

---

# ナビゲーション{#navigation}

インタラクティブビデオビューア用のURLコマンド。

` navigation= *`ファイル`*`

ビューアでは、ホストされているWebVTTファイルによるビデオチャプターナビゲーションがサポートされています。 キュー位置の演算子はサポートされていません。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTTナビゲーションコンテンツのURLまたはパスを指定します。 画像サービングはWebVTTファイルをホストする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

なし

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```

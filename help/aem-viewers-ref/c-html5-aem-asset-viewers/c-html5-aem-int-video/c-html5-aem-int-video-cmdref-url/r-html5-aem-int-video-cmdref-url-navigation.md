---
description: インタラクティブビデオビューア用のURLコマンド。
solution: Experience Manager
title: ナビゲーション
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブビデオ
role: Developer,User
exl-id: 9852e723-fd1f-4ade-921b-cfb92bf9f2ad
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 12%

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

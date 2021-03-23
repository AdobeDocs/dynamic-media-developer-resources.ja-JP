---
description: インタラクティブビデオビューアのURLコマンド
seo-description: インタラクティブビデオビューアのURLコマンド
seo-title: ナビゲーション
solution: Experience Manager
title: ナビゲーション
uuid: eecc7458-153c-4f36-b29e-97451f275c0c
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 12%

---


# ナビゲーション{#navigation}

インタラクティブビデオビューアのURLコマンド

` navigation= *`ファイル`*`

ビューアでは、ホストされているWebVTTファイルによるビデオチャプターナビゲーションがサポートされています。 キュー位置の演算子はサポートされていません。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTTナビゲーションコンテンツへのURLまたはパスを指定します。 画像サービングはWebVTTファイルをホストする必要があります。 </p> </td> 
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


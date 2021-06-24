---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブビデオ
role: Developer,Business Practitioner
exl-id: 75ee2c74-21c4-41b6-9d0f-15aa8432f177
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

インタラクティブビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> デスクトップでのビデオの初期再生に使用するビデオビットレート(kbps)を設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは次に低いビットレートのビデオで開始します。 </p> <p><span class="codeph"> 0</span>に設定すると、ビデオプレーヤーは最も低いビットレートから開始します。 </p> <p>HTML5 HLSビデオをネイティブでサポートしていないシステム（Windows 10のFirefox、Chrome、Internet Explorer 11ブラウザーなど）で再生モードがautoに設定されている場合にのみ適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```

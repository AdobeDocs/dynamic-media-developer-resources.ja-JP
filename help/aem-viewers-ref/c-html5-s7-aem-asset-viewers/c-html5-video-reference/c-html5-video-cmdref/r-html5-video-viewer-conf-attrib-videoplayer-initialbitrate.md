---
description: ビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ
role: Developer,Business Practitioner
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

ビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value  </span> </p> </td> 
   <td colname="col2"> <p>デスクトップでのビデオの初期再生に使用する、ビデオのビットレート(kbps)を設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは次に低いビットレートを持つビデオを開始します。 </p> <p><span class="codeph"> 0 </span>に設定した場合、ビデオプレーヤーは可能な限り低いビットレートから開始します。 HTML5 HLSビデオ（Windows 10のFirefox、Chrome、Internet Explorer 11ブラウザー）をネイティブでサポートしていないシステムで、再生モードが<span class="codeph"> auto </span>に設定されている場合にのみ適用されます。 </p> </td> 
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

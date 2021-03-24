---
description: ビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Mediaクラシック，ビューア，SDK/API，ビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

ビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value  </span> </p> </td> 
   <td colname="col2"> <p>デスクトップでのビデオの初期再生に使用する、ビデオのビットレート（キロビット/秒、kbps）を設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは次に低いビットレートを持つビデオを開始します。 </p> <p><span class="codeph"> 0 </span>に設定した場合、ビデオプレーヤー開始は最も低いビットレートから取得されます。 HTML5 HLSビデオ（Windows 10のFirefox、Chrome、Internet Explorer 11ブラウザー）をネイティブサポートしていないシステム、および再生モードが<span class="codeph"> auto </span>に設定されている場合にのみ適用できます。 </p> </td> 
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


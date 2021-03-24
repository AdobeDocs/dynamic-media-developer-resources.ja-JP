---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Mediaクラシック，ビューア，SDK/API，混在メディアセット
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p>デスクトップでのビデオの初期再生に使用する、ビデオのビットレート（キロビット/秒、kbps）を設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは次に低いビットレートを持つビデオを開始します。 </p> <p><span class="codeph"> 0 </span>に設定した場合、ビデオプレーヤー開始は最も低いビットレートから取得されます。 HTML5 HLSビデオ（Windows 10のFirefox、Chrome、Internet Explorer 11ブラウザー）をネイティブサポートしていないシステム、および再生モードが<span class="codeph"> auto </span>に設定されている場合にのみ適用できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`

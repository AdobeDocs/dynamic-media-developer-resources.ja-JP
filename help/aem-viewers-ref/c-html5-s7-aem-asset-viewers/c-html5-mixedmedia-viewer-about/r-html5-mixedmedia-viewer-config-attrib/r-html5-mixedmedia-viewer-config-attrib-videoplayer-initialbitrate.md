---
description: 'null'
seo-description: 'null'
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: 11426516-8336-4186-84b4-15ce5ec7e764
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 価 </span> 値 </span> </p> </td> 
   <td colname="col2"> <p>デスクトップでのビデオの初期再生に使用するビデオのビットレート(kbps)を設定します。 </p> <p>このビットレート値がアダプティブビデオセットに存在しない場合、ビデオプレーヤーは次に低いビットレートのビデオを開始します。 </p> <p>0に設定すると、ビ <span class="codeph"> デオプレ </span> ーヤーは最も低いビットレートから開始されます。 HTML5 HLSビデオ（Windows 10のFirefox、Chrome、Internet Explorer 11の各ブラウザー）をネイティブでサポートしていないシステムで、再生モードが自動に設定されている場合にのみ適用され <span class="codeph"> ます </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`

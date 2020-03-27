---
description: 'null'
seo-description: 'null'
seo-title: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic media
uuid: 94de31cd-2b4e-4247-b181-26666767f065
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> 現在のシステムでアダプティブビデオの再生がサポートされていない場合に、アダプティブビデオセットから再生するビデオのビットレート（キロビット/秒またはkbps）を指定します。 </p> <p>コンポーネントは、指定された値に可能な限り近い（ただし、超えない）ビットレートでビデオストリームを取得します。 アダプティブビデオセット内のすべてのビデオストリームの画質が指定値より高い場合、ロジックは最も低い画質のビットレートを選択します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`

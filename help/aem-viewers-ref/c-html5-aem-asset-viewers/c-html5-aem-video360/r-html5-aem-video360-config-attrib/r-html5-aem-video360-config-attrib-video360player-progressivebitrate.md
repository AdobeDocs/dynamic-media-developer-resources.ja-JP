---
description: ビデオ360ビューアの設定属性。
seo-description: ビデオ360ビューアの設定属性。
seo-title: Video360Player.progressivebitrate
solution: Experience Manager
title: Video360Player.progressivebitrate
topic: Dynamic media
uuid: 438c18d7-e7ac-4834-8445-def590264448
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.progressivebitrate{#video-player-progressivebitrate}

ビデオ360ビューアの設定属性。

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> 現在のシステムでアダプティブビデオの再生がサポートされていない場合に、アダプティブビデオセットから再生するビデオのビットレート(kbps)単位で指定します。 </p> <p>コンポーネントは、指定された値に可能な限り近い（ただし、超えない）ビットレートでビデオストリームを取得します。 アダプティブビデオセット内のすべてのビデオストリームの画質が指定値より高い場合は、最も低い画質のビットレートが選択されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```


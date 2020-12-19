---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: dc2e7b18-abd7-4b53-a0c4-268ec9cf3cb4
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

インタラクティブビデオビューアの設定属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 時間の吹き出しに表示する時間のパターンを設定します。<span class="codeph"> h</span>は時間を表し、<span class="codeph"> m</span>は分を表し、<span class="codeph"> s</span>は秒を表します。 </p> <p>各時間単位に使用される文字数によって、その単位に表示する桁数が決まります。 指定した桁数に収まらない場合は、後続の単位に相当する値が表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、<span class="codeph"> m:ss</span>は67:05と表示されます。 時間パターンが<span class="codeph"> h:mm:s</span>の場合は、1:07:5と同じ時間が表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```


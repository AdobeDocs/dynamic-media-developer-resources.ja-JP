---
description: ビデオビューアの設定属性。
solution: Experience Manager
title: VideoScrubber.timepattern
feature: Dynamic Mediaクラシック，ビューア，SDK/API，ビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

ビデオビューアの設定属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 時間の吹き出しに表示する時間のパターンを設定します。<span class="codeph"> h</span>は時間、<span class="codeph"> m</span>は分、<span class="codeph"> s</span>は秒を表します。 </p> <p>各時間単位に使用される文字数によって、その単位に表示する桁数が決まります。 指定した桁数に収まらない場合は、後続の単位に相当する値が表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、時間パターン<span class="codeph"> m:ss</span>は67:05と表示されます。 指定した時間パターンが<span class="codeph"> h:mm:s</span>の場合、同じ時間が1:07:5と表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```


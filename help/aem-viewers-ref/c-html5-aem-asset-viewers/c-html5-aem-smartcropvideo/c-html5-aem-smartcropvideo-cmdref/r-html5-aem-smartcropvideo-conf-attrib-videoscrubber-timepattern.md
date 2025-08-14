---
title: VideoScrubber.timepattern
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 4b3082f6-fb88-4c69-ab09-e24cff039222
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

スマート切り抜きビデオビューアの設定属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> タイムバブルに表示される時間のパターンを設定します。<span class="codeph"> h</span> は時間、<span class="codeph"> m</span> は分、<span class="codeph"> s</span> は秒です。 </p> <p>時間単位ごとに使用される文字数によって、その単位に表示する桁数が決まります。 数値が指定の数字に収まらない場合は、対応する値が後続の単位で表示されます。 </p> <p>例えば、現在のムービーの時間が 67 分 5 秒の場合、タイムパターン <span class="codeph">m:ss</span> は 67:05 と表示されます。 指定した時間パターンが :07: h<span class="codeph">s:mm: の場合は、同じ時間が 1</span>5 と表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```

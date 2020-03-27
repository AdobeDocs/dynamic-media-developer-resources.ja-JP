---
description: ビデオ360ビューアの設定属性。
seo-description: ビデオ360ビューアの設定属性。
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: 73651147-d122-4466-ad74-e5f9438a9c56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

ビデオ360ビューアの設定属性。

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 時間の吹き出しに表示する時間のパターンを設定します。 <span class="codeph"> hは時間</span> 、 <span class="codeph"> mは分、</span> sは秒 <span class="codeph"></span> です。 </p> <p>各時間単位で使用される文字の数によって、その単位に表示する桁数が決まります。 数値が指定の桁数に収まらない場合は、対応する値が後続の単位で表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、時間パターン <span class="codeph"> m:ss</span> は67:05と表示されます。 指定した時間パターンがh:mm:sの場合、同じ時間は1:07:5と表 <span class="codeph"> 示されます</span>。 </p> </td> 
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


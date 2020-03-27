---
description: 'null'
seo-description: 'null'
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: 6034dc22-c1d4-4a37-93de-42a88b99234a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 時間の吹き出しに表示する時間のパターンを設定します。 <span class="codeph"> hは時間</span> 、 <span class="codeph"> mは分、</span> sは秒 <span class="codeph"></span> です。 </p> <p>各時間単位で使用される文字の数によって、その単位に表示する桁数が決まります。 数値が指定の桁数に収まらない場合は、対応する値が後続の単位で表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、時間パターン <span class="codeph"> m:ss</span> は67:05と表示されます。 指定した時間パターンがh:mm:sの場合、同じ時間は1:07:5と表 <span class="codeph"> 示されます</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`

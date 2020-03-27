---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: 90d36f73-44f9-4e4e-9ad6-e866749f9b2f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoTime.timepattern{#videotime-timepattern}

インタラクティブビデオビューアの設定属性。

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーに表示する時間のパターンを設定します。 <span class="codeph"> hは時間</span> 、 <span class="codeph"> mは分、sは秒を表</span> します <span class="codeph"></span> 。 </p> <p>各時間単位で使用される文字の数によって、その単位に表示する桁数が決まります。 数値が指定の桁数に収まらない場合は、対応する値が後続の単位で表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、 <span class="codeph"> m:ssの時間パターンは</span> 67:05と表示されます。 時間パターンがh:mm:sの場合、同じ時間は1:07:5と表 <span class="codeph"> 示されます</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```


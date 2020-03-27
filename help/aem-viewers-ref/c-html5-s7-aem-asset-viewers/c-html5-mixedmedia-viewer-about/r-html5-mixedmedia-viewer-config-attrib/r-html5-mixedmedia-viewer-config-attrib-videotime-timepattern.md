---
description: 'null'
seo-description: 'null'
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: 57c86b63-7495-4f6f-bd30-8c4ebf017e36
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーに表示する時間のパターンを設定します。 <span class="codeph"> hは時間</span> 、 <span class="codeph"> mは分、</span> sは秒 <span class="codeph"></span> です。 </p> <p>各時間単位で使用される文字の数によって、その単位に表示する桁数が決まります。 数値が指定の桁数に収まらない場合は、対応する値が後続の単位で表示されます。 </p> <p>例えば、現在のムービー時間が67分5秒の場合、時間パターン <span class="codeph"> m:ss</span> は67:05と表示されます。 指定した時間パターンがh:mm:sの場合、同じ時間は1:07:5と表 <span class="codeph"> 示されます</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`

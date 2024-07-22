---
title: VideoPlayer.iconeffect
description: VideoPlayer.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 8371cb69-4cd9-457b-bd8c-e4167fc67600
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> ビデオが一時停止されたときに、ビデオの上に IconEffect を表示できるようにします。 一部のデバイスでは、ネイティブコントロールが使用されます。 この場合、<span class="codeph"> iconeffect</span> 修飾子は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffect が表示および再表示される最大回数を指定します。 値 <span class="codeph">-1</span> は、アイコンが無限に再び表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p> アニメーションの表示または非表示の時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffect が自動的に非表示になるまでの秒数を設定します。 つまり、フェードイン アニメーションが完了してからフェードアウト アニメーションが開始するまでの時間です。 0</span> に設定 <span class="codeph"> ると、自動非表示動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`

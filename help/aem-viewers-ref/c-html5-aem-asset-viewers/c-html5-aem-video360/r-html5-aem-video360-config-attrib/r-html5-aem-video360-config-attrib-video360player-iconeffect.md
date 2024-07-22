---
title: Video360Player.iconeffect
description: Video360 ビューアの設定属性
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# Video360Player.iconeffect{#video-player-iconeffect}

Video360 ビューアの設定属性

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> ビデオが一時停止の状態にあるときに、ビデオの上に IconEffect を表示できるようにします。 一部のデバイスでは、ネイティブコントロールが使用されます。 このような場合、<span class="codeph">iconeffect</span> 修飾子は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数 </span></span> </p> </td> 
   <td colname="col2"> <p> IconEffect が表示および再表示される最大回数を指定します。 値 <span class="codeph">-1</span> は、アイコンが無限に再び表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> フェード </span></span> </p> </td> 
   <td colname="col2"> <p> アニメーションの表示または非表示の時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffect が自動的に非表示になるまでに完全に表示される秒数を設定します。 つまり、フェードイン アニメーションが完了してからフェードアウト アニメーションが開始するまでの時間です。 <span class="codeph"> 0</span> に設定すると、自動非表示動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`

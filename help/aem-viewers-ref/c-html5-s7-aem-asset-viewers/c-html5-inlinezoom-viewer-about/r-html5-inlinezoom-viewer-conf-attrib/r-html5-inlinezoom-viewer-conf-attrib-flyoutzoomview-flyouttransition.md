---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 3199d4a3-4799-40a2-b0a5-0e1ee4744fbe
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`showtime`*[, *`showdelay`*[, *`hidetime`*[, *`hidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|スライド|フェード </span> </span> </p> </td> 
   <td colname="col2"> <p> フライアウト ビューを表示または非表示にするときに適用する効果のタイプを指定します。 <span class="codeph"> none </span> を指定すると、フライアウト画像はアクティブ化されて準備が整うと即座に表示されます。スライド </span> を指定す <span class="codeph"> と、スライドアニメーションが左から右の方向に再生されます。<span class="codeph"> fade </span> を指定すると、フライアウト画像にアルファ遷移が適用されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> アニメーション表示が完了するまでにかかる秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span> </span> </p> </td> 
   <td colname="col2"> <p> アニメーションの表示を開始するユーザー操作と、アニメーションの表示自体の開始との間の遅延（秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime </span> </span> </p> </td> 
   <td colname="col2"> <p> 非表示のアニメーションが完了するまでにかかる秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span> </span> </p> </td> 
   <td colname="col2"> <p> 非表示のアニメーションを開始するユーザ アクションと、非表示のアニメーション自体の開始との間の遅延（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

オプション。

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`

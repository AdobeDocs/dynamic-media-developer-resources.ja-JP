---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 39cb629a-3940-4206-91cd-fe9a9f4d9f75
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`期間`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> アセットの変更時にメインビューに適用される効果のタイプを指定します。 </p> <p><span class="codeph"> なし</span> を指定すると、トランジションなしで、メインビューの変更が即座に行われます。 </p> <p><span class="codeph"> フェード</span> クロスフェードトランジションを有効にし、古い画像がフェードアウトして新しい画像がフェードインします。 </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p> アニメーションが完了するまでの時間（秒）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

なし

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`

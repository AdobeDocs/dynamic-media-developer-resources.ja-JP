---
description: FlyoutZoomView.frametransition
solution: Experience Manager
title: FlyoutZoomView.frametransition
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,User
exl-id: 39cb629a-3940-4206-91cd-fe9a9f4d9f75
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 10%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`期間`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> アセットの変更時にメインビューに適用される効果のタイプを指定します。 </p> <p><span class="codeph"> </span> nonesは、トランジションなしを表し、メインビューの変更は即座におこなわれます。 </p> <p><span class="codeph"> </span> fadeを指定すると、クロスフェードトランジションが有効になり、古い画像がフェードアウトして新しい画像がフェードインします。 </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p> アニメーションの完了に要する秒数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

なし

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`

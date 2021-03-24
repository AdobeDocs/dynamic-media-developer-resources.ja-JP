---
description: FlyoutZoomView.frametransition
solution: Experience Manager
title: FlyoutZoomView.frametransition
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インラインズーム
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---


# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`期間`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> アセットの変更時にメイン表示に適用する効果のタイプを指定します。 </p> <p><span class="codeph"> トランジション</span> を行わないと、メイン表示の変更が即座に発生します。 </p> <p><span class="codeph"> fadeを指定すると、クロスフェードトランジションが有効になります。この画像では、古い画像がフェードアウトし、新しい画像がフェードインします。</span>  </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p> アニメーションが完了するまでの秒数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

なし

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`

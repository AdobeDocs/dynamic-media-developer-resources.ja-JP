---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> サイズ変更時にコンポーネントがメインおよびフライアウトビュー用の新しい画像を取得する方法を設定します。 </p> <p><span class="codeph"> 0</span> に設定すると、コンポーネントはサイズ変更時に新しい画像を読み込まず、フライアウトビューの画像の解像度も変更されません。 </p> <p><span class="codeph">1 に設定すると </span> メインビューに読み込む画像の幅のブレークポイントを 1 つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ブレークポイント、<span class="varname"> 幅 </span>、<span class="varname"> 幅 </span> </span> </p> </td> 
   <td colname="col2"> <p>メインビューに読み込まれる画像の幅のブレークポイント。 </p> <p>このコンポーネントは、初期負荷に最適なサイズを常に使用します。 サイズ変更後、メインビューの画像は、最も近い大きいブレークポイントに等しい幅を使用して常にダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

オプション。

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`

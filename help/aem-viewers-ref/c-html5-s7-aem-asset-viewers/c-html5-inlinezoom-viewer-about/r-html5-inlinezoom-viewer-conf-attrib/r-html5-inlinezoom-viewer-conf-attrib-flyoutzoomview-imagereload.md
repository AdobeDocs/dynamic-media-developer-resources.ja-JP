---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`幅`*[; *`幅`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> コンポーネントがサイズ変更時にメインビューとフライアウトビューの新しい画像を取得する方法を設定します。 </p> <p>に設定 <span class="codeph"> 0 </span>の場合、コンポーネントはサイズ変更時に新しい画像を読み込まず、フライアウトビューの画像解像度は変更されません。 </p> <p>に設定 <span class="codeph"> 1 </span> メインビューに読み込まれる画像の幅のブレークポイントを 1 つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ブレークポイント <span class="varname"> 幅 </span>; <span class="varname"> 幅 </span> </span> </p> </td> 
   <td colname="col2"> <p>メインビューに読み込まれる画像の幅のブレークポイント。 </p> <p>コンポーネントは、常に最初の読み込みに最適なサイズを使用します。 サイズ変更後は、メインビューの画像が常に最も近い大きいブレークポイントと等しい幅を使用してダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`

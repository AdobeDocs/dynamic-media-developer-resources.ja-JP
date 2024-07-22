---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> サイズ変更時にコンポーネントがメインおよびフライアウトビュー用の新しい画像を取得する方法を設定します。 </p> <p><span class="codeph"> 0 </span> に設定すると、コンポーネントはサイズ変更時に新しい画像を読み込みません。フライアウトビューの画像の解像度は変更されません。 </p> <p><span class="codeph"> 1 </span> に設定すると、メインビューに読み込む画像の幅のブレークポイントを 1 つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ブレークポイント、<span class="varname"> 幅 </span>[; <span class="varname"> 幅 </span>] </span> </p> </td> 
   <td colname="col2"> <p> メインビューに読み込まれる画像の幅のブレークポイント。 このコンポーネントは、初期負荷に最適なサイズを常に使用します。 サイズ変更後、メインビューの画像は常に最も近い大きいブレークポイントに等しい幅でダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`

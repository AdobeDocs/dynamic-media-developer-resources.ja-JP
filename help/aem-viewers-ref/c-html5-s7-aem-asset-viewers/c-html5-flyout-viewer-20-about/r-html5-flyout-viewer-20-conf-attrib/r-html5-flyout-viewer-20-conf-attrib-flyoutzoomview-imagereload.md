---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic，ビューア，SDK/API，フライアウト
role: Developer,Business Practitioner
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`widthwidth`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> サイズ変更時にメインビューとフライアウトビューの新しい画像を取得する方法を設定します。 </p> <p><span class="codeph"> 0 </span>に設定すると、コンポーネントはサイズ変更時に新しい画像を読み込みません。フライアウトビューの画像解像度は変更されません。 </p> <p><span class="codeph"> 1 </span>に設定すると、メインビューにロードされる画像の幅のブレークポイントを1つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breakpoint,  <span class="varname"> width  </span>[; <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p> メインビューに読み込まれる画像の幅のブレークポイント。 コンポーネントは、常に最初の荷重に最適なサイズを使用します。 サイズ変更後は、メインビュー内の画像が常に最も近い大きなブレークポイントと等しい幅でダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`

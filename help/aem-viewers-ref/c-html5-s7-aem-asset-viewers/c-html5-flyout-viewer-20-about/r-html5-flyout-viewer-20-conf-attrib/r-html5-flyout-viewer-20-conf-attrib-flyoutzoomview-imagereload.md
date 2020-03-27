---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 1de87e2f-5cb9-406a-96bc-3486c2592951
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`幅`*[; *`幅`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> コンポーネントがサイズ変更時にメインビューとフライアウトビューの新しい画像を取得する方法を設定します。 </p> <p>0に設定した場 <span class="codeph"> 合、コ </span>ンポーネントはサイズ変更時に新しい画像を読み込みません。フライアウトビューの画像解像度は変更されません。 </p> <p>1に設定す <span class="codeph"> ると、 </span> メインビューに読み込まれる画像の幅のブレークポイントを1つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breakpoint、 <span class="varname"> width </span>[; <span class="varname"> 幅 </span>] </span> </p> </td> 
   <td colname="col2"> <p> メインビューに読み込まれる画像の幅のブレークポイント。 コンポーネントは、常に最初の荷重に最適なサイズを使用します。 サイズ変更後は、メインビューの画像が常に最も近い大きいほうのブレークポイントと同じ幅でダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`

---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 1de87e2f-5cb9-406a-96bc-3486c2592951
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`幅`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> コンポーネントで、サイズ変更時にメイン画像とフライアウト表示の新しい画像を取得する方法を設定します。 </p> <p><span class="codeph"> 0 </span>に設定した場合、コンポーネントはサイズ変更時に新しい画像を読み込みません。フライアウト表示の画像解像度は変更されません。 </p> <p><span class="codeph"> 1 </span>に設定すると、メイン表示にロードする画像の幅のブレークポイントを1つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breakpoint,  <span class="varname"> width  </span>[; <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p> メイン表示に読み込まれる画像の幅のブレークポイント。 コンポーネントでは、常に最初の読み込みに最適なサイズが使用されます。 サイズ変更後、メイン表示内の画像は常に最も近い大きいほうのブレークポイントと等しい幅でダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`

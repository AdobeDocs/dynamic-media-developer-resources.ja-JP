---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インラインズーム
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`幅`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> コンポーネントで、サイズ変更時にメイン画像とフライアウト表示の新しい画像を取得する方法を設定します。 </p> <p><span class="codeph"> 0 </span>に設定すると、コンポーネントはサイズ変更時に新しい画像を読み込まず、フライアウト表示の画像解像度は変更されません。 </p> <p><span class="codeph"> 1 </span>に設定すると、メイン表示にロードする画像の幅のブレークポイントを1つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breakpoint,  <span class="varname"> width  </span>; <span class="varname"> width  </span> </span> </p> </td> 
   <td colname="col2"> <p>メイン表示に読み込まれる画像の幅のブレークポイント。 </p> <p>コンポーネントでは、常に最初の読み込みに最適なサイズが使用されます。 サイズ変更後は、メイン表示の画像が常に最も近い大きいほうのブレークポイントと等しい幅でダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`

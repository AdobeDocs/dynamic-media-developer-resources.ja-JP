---
title: FlyoutZoomView.imagereload
description: コンポーネントがサイズ変更時にメインビューとフライアウトビューの新しい画像を取得する方法を設定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

コンポーネントがサイズ変更時にメインビューとフライアウトビューの新しい画像を取得する方法を設定します。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`幅`*[; *`幅`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>に設定する場合 <span class="codeph"> 0 </span>の場合、コンポーネントはサイズ変更時に新しい画像を読み込まず、フライアウトビューの画像解像度は変更されません。 </p> <p>に設定する場合 <span class="codeph"> 1 </span> メインビューに読み込まれる画像の幅のブレークポイントを 1 つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ブレークポイント <span class="varname"> 幅 </span>[; <span class="varname"> 幅 </span>] </span> </p> </td> 
   <td colname="col2"> <p>メインビューに読み込まれる画像の幅のブレークポイント。 コンポーネントは、常に最初の読み込みに最適なサイズを使用します。 サイズ変更後は、メインビューの画像が常に最も近い大きいブレークポイントと等しい幅でダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`

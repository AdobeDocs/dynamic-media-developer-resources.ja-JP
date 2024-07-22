---
title: FlyoutZoomView.imagereload
description: サイズ変更時にコンポーネントがメインおよびフライアウトビュー用の新しい画像を取得する方法を設定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

サイズ変更時にコンポーネントがメインおよびフライアウトビュー用の新しい画像を取得する方法を設定します。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 0 </span> に設定すると、コンポーネントはサイズ変更時に新しい画像を読み込まず、フライアウトビューの画像の解像度も変更されません。 </p> <p><span class="codeph"> 1 に設定すると、メイン ビュ </span> に読み込むイメージに対して、幅のブレークポイントを 1 つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ブレークポイント、<span class="varname"> 幅 </span>[; <span class="varname"> 幅 </span>] </span> </p> </td> 
   <td colname="col2"> <p>メインビューに読み込まれた画像の幅のブレークポイント。 コンポーネントは、初期負荷に常に最適フィット サイズを使用します。 サイズ変更後、メインビューの画像は常に最も近い大きいブレークポイントに等しい幅でダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`

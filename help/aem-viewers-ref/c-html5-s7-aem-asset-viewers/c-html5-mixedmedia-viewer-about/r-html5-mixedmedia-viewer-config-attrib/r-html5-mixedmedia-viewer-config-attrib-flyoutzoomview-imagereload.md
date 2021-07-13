---
description: サイズ変更時にメインビューとフライアウトビューの新しい画像を取得する方法を設定します。
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

サイズ変更時にメインビューとフライアウトビューの新しい画像を取得する方法を設定します。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`widthwidth`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 0 </span>に設定した場合、コンポーネントはサイズ変更時に新しい画像を読み込まず、フライアウトビューの画像解像度は変更されません。 </p> <p><span class="codeph"> 1 </span>に設定すると、メインビューにロードされる画像の幅のブレークポイントを1つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breakpoint,  <span class="varname"> width  </span>[; <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p>メインビューに読み込まれる画像の幅のブレークポイント。 コンポーネントは、常に最初の荷重に最適なサイズを使用します。 サイズ変更後は、メインビューの画像が常に最も近い大きいブレークポイントと等しい幅でダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`

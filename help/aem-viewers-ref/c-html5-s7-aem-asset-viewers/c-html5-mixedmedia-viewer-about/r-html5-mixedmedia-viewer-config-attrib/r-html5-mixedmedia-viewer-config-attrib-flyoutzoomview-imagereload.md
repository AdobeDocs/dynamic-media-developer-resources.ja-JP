---
description: コンポーネントで、サイズ変更時にメイン画像とフライアウト表示の新しい画像を取得する方法を設定します。
seo-description: コンポーネントで、サイズ変更時にメイン画像とフライアウト表示の新しい画像を取得する方法を設定します。
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 5cded4cb-7b02-47da-9e2d-b236548cc61d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 3%

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

コンポーネントで、サイズ変更時にメイン画像とフライアウト表示の新しい画像を取得する方法を設定します。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`幅`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 0 </span>に設定した場合、コンポーネントはサイズ変更時に新しい画像を読み込まず、フライアウト表示の画像解像度は変更されません。 </p> <p><span class="codeph"> 1 </span>に設定すると、メイン表示にロードする画像の幅のブレークポイントを1つ以上指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breakpoint,  <span class="varname"> width  </span>[; <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p>メイン表示に読み込まれる画像の幅のブレークポイント。 コンポーネントは、最初の読み込みに常に最適なサイズを使用します。 サイズ変更後は、メイン表示の画像が常に最も近い大きいブレークポイントと等しい幅でダウンロードされ、クライアント上で縮小されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`

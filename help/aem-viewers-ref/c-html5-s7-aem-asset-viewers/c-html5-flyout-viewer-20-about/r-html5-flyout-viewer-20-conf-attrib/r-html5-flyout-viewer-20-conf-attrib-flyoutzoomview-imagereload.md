---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
TQID: 'https://experienceleague.adobe.com/nkYQwtTb1AUBLBbnN2HwMZLIjyolj5l-6CxEy-yEo3k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> サイズ変更時に、コンポーネントがメインビューとフライアウトビューの新しい画像を取得する方法を設定します。 </p> <p><span class="codeph"> 0 </span>に設定した場合、コンポーネントはサイズ変更時に新しい画像を読み込みません。フライアウトビューの画像解像度は変更されません。 </p> <p><span class="codeph"> 1 </span>に設定すると、メインビューに読み込まれる画像の1つ以上の幅ブレークポイントを指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ブレークポイント、<span class="varname">幅</span>[; <span class="varname">幅</span>] </span> </p> </td> 
   <td colname="col2"> <p> メインビューに読み込まれる画像の幅ブレークポイント。 コンポーネントは常に初期負荷に最適なサイズを使用します。 サイズ変更後は、メインビュー内の画像が、最も大きなブレークポイントに等しい幅で常にダウンロードされ、クライアント上でダウンスケールされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`

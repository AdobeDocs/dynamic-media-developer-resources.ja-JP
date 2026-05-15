---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
TQID: 'https://experienceleague.adobe.com/utzPqD5UMx7TnJK8FvqflzoSjOWGVaGXhKlviY1U9xQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> サイズ変更時に、コンポーネントがメインビューとフライアウトビューの新しい画像を取得する方法を設定します。 </p> <p><span class="codeph"> 0 </span>に設定すると、コンポーネントはサイズ変更時に新しい画像を読み込まず、フライアウトビューの画像解像度は変更されません。 </p> <p><span class="codeph"> 1 </span>に設定すると、メインビューに読み込まれる画像の1つ以上の幅ブレークポイントを指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ブレークポイント、<span class="varname">幅</span>、<span class="varname">幅</span> </span> </p> </td> 
   <td colname="col2"> <p>メインビューに読み込まれる画像の幅ブレークポイント。 </p> <p>コンポーネントは常に初期負荷に最適なサイズを使用します。 サイズを変更すると、メインビュー内の画像が、最も近い大きなブレークポイントに等しい幅を使用して常にダウンロードされ、クライアントでダウンスケールされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

オプション。

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`

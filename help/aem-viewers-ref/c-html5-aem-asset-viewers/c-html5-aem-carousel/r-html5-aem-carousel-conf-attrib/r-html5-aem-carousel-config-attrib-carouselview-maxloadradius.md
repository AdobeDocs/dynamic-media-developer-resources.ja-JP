---
title: CarouselView.maxloadradius
description: CarouselView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph"> -1</span>に設定すると、コンポーネントはアイドル状態のときにすべてのカルーセルフレームをプリロードします。 </p> <p><span class="codeph"> 0</span>に設定すると、コンポーネントは現在表示されているフレーム、前のフレーム、次のフレームのみを読み込みます。 </p> <p><span class="codeph"><span class="varname"> </span></span>preloadnbrは、アイドル状態の場合に、現在表示されているフレームの周囲にある非表示のフレームの数を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`

---
title: CarouselView.autoplay
description: カルーセルビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# CarouselView.autoplay{#carouselview-autoplay}

カルーセルビューアの設定属性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duration][,direction]</span> </p> </td> 
   <td colname="col2"> <p> オン/オフ、カルーセルに各バナーを表示する時間および自動ループの方向を指定します。 </p> <p>自動ループをオフにするには、<span class="codeph"> 0</span> に設定します。 </p> <p><span class="codeph"> 1</span> を自動ループ オンに設定し、トランジションのデュレーション（秒単位）を <span class="codeph"> duration</span> で制御します。 </p> <p>自動ループの方向は、<span class="codeph"> 方向 </span> で制御されます。 <span class="codeph"> 方向 </span> の範囲は <span class="codeph"> 1</span> 右から左と <span class="codeph"> 0</span> 左から右です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,9`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```

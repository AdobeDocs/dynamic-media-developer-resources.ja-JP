---
description: カルーセルビューアの設定属性。
seo-description: カルーセルビューアの設定属性。
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
topic: Dynamic media
uuid: 12730b17-110e-405b-97fe-e70fab89c703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.autoplay{#carouselview-autoplay}

カルーセルビューアの設定属性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duration][,direction]</span> </p> </td> 
   <td colname="col2"> <p> カルーセル内の各バナーの表示時間と、自動ループの方向をオン/オフで指定します。 </p> <p>自動ループをオ <span class="codeph"> フにする</span> には、0に設定します。 </p> <p>1をオ <span class="codeph"> ートループ</span> オンに設定し、トランジション時間を秒単位で時間で制御 <span class="codeph"> します</span>。 </p> <p>自動ループの方向は、方向で制御し <span class="codeph"> ます</span>。 方向 <span class="codeph"> は</span> 、右から左に1 <span class="codeph"> 、左から右</span> に0 <span class="codeph"></span> の範囲で指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,9`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```


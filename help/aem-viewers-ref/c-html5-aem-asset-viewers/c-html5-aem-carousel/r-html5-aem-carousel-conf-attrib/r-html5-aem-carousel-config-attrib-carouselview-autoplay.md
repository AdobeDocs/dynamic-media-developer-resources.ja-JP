---
description: カルーセルビューアの設定属性。
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Mediaクラシック，ビューア，SDK/API，カルーセルバナー
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---


# CarouselView.autoplay{#carouselview-autoplay}

カルーセルビューアの設定属性。

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duration][,direction]</span> </p> </td> 
   <td colname="col2"> <p> カルーセルに各バナーを表示するオン/オフ（時間）と、自動ループの方向を指定します。 </p> <p><span class="codeph"> 0</span>に設定すると、自動ループがオフになります。 </p> <p><span class="codeph"> 1</span>を、<span class="codeph"> duration</span>で制御されるトランジション時間（秒）で自動ループオンに設定します。 </p> <p>オートループの方向は<span class="codeph">方向</span>で制御します。 <span class="codeph">方向</span>は、<span class="codeph"> 1</span>右から左、<span class="codeph"> 0</span>左から右の範囲です。 </p> </td> 
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


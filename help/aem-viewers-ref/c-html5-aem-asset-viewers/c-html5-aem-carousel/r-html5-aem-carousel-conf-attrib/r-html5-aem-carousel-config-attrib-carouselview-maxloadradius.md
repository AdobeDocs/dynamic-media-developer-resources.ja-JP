---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
feature: Dynamic Mediaクラシック，ビューア，SDK/API，カルーセルバナー
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph"> -1</span>に設定すると、コンポーネントはアイドル状態のときにすべてのカルーセルフレームをプリロードします。 </p> <p><span class="codeph"> 0</span>に設定すると、コンポーネントは現在表示されているフレーム、前のフレーム、次のフレームのみを読み込みます。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>は、アイドル状態の場合に、現在表示されているフレームの前後にある非表示のフレームをいくつプリロードするかを定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`

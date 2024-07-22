---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`duration`*[, *`spacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|フェード|スライド </span> </p> </td> 
   <td colname="col2"> <p>フレーム変更時に適用する効果のタイプを指定します。 例えば、<span class="codeph"> none </span> はトランジションを表しません。フレームの変更は即座に行われます。 また、 </p> <p> フェード </span> ード <span class="codeph">、古いフレームと新しいフレームの間のクロスフェードトランジションを意味します。 最後に </p> <p> <span class="codeph"> のスライド </span> は、古いフレームがビューからスライドし、新しいフレームがスライドするトランジションをアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
   <td colname="col2"> <p>フェード </span> またはスライド切り替え効果 <span class="codeph"> デュレーション （秒） <span class="codeph"> 指定 </span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spacing </span> </span> </p> </td> 
   <td colname="col2"> <p>スライド </span> トランジション内の隣接 <span class="codeph"> るフレーム間の間隔は、0 </span> ～ <span class="codeph"> 1 </span> の範囲 <span class="codeph"> あり、コンポーネントの幅に対して相対的です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`

---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
topic: Dynamic media
uuid: 9539ede1-08fb-4bfc-8a5a-870c7d84de7f
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 5%

---


# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`durationspacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide  </span> </p> </td> 
   <td colname="col2"> <p>フレーム変更時に適用する効果のタイプを指定します。 <span class="codeph"> none </span> はトランジションなしを表します。フレームの変更はすぐに行われます。 </p> <p> <span class="codeph"> fadeは、前のフレームと次のフレームの間にクロスフェードトランジションを適用する </span> ことを意味します。 </p> <p> <span class="codeph"> slideは、前のフレームを表示からスライドアウトし、新しいフレームをスライドインするトランジションを </span> アクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> fade </span>または<span class="codeph"> slide </span>トランジション効果の時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spacing  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">スライド</span>トランジション内の隣接するフレーム間の間隔。<span class="codeph"> 0 </span> ～ <span class="codeph"> 1 </span>の範囲を持ち、コンポーネントの幅を基準にして指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`

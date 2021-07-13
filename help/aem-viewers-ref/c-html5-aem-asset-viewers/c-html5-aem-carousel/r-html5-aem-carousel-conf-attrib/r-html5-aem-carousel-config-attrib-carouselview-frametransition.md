---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
feature: Dynamic Media Classic，ビューア，SDK/API，カルーセルバナー
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 5%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`durationspacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide  </span> </p> </td> 
   <td colname="col2"> <p>フレームの変更時に適用する効果のタイプを指定します。 <span class="codeph"> none </span> は、移行なしを表します。フレームの変更はすぐに行われます。 </p> <p> <span class="codeph"> fadeは、前のフ </span> レームと次のフレームの間にクロスフェードのトランジションを設定します。 </p> <p> <span class="codeph"> slideは、 </span> 前のフレームがビューからスライドアウトし、新しいフレームがスライドインするトランジションをアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">フェード</span>または<span class="codeph">スライド</span>のトランジション効果の時間（秒単位）を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spacing  </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">スライド</span>トランジション内の隣接するフレーム間の間隔は、<span class="codeph"> 0 </span>と<span class="codeph"> 1 </span>の間の範囲で、コンポーネントの幅を基準にした値です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`

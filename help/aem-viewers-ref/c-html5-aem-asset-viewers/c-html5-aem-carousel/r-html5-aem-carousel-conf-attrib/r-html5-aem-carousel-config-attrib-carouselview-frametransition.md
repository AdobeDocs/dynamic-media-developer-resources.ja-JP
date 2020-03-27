---
description: 'null'
seo-description: 'null'
seo-title: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
topic: Dynamic media
uuid: 9539ede1-08fb-4bfc-8a5a-870c7d84de7f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`間隔(`*[, *`長)`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide </span> </p> </td> 
   <td colname="col2"> <p>フレーム変更時に適用する効果のタイプを指定します。 <span class="codeph"> noneは、 </span> 移行なしを表します。フレームの変更はすぐに行われます。 </p> <p> <span class="codeph"> fadeは、前の </span> フレームと次のフレームの間のクロスフェードトランジションを意味します。 </p> <p> <span class="codeph"> slideは、前 </span> のフレームがビューからスライドアウトし、新しいフレームがスライドインするトランジションをアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 期 </span> 間 </span> </p> </td> 
   <td colname="col2"> <p>フェードまたはスライドのトランジション効果の時 <span class="codeph"> 間（秒） </span> を <span class="codeph"> 指定 </span> します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 間 </span> 隔 </span> </p> </td> 
   <td colname="col2"> <p>スライドトランジションで隣接す <span class="codeph"> るフ </span> レーム間の間隔。0 ～ <span class="codeph"> 1 </span> の範 <span class="codeph"> 囲で、コンポーネ </span> ントの幅に対する相対値を指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

なし

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`

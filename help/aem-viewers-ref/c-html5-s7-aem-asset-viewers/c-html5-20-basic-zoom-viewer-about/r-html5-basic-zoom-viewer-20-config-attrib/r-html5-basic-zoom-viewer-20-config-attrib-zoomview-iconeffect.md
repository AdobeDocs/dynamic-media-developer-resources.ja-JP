---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
topic: Dynamic media
uuid: 38350e3d-515b-454c-bc85-39b91ad06e8b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`countfadeautoHide`*][, *``*][, *``*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態で、画像の操作に使用できるアクションが示されている場合に、IconEffectを画像の上部に表示できるようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 数</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectの表示と再表示の最大回数を指定します。 値が —1の場合、ア <span class="codeph"> イコンは</span> 常に無限に再表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フェー <span class="varname"> ド</span></span> </p> </td> 
   <td colname="col2"> <p>表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動非 <span class="varname"> 表示</span></span> </p> </td> 
   <td colname="col2"> <p>IconEffectが完全に表示された状態で、自動非表示になるまでの秒数を設定します。 つまり、フェードインアニメーションが完了してからフェードアウトアニメーションが開始するまでの時間です。 0に設定すると、自 <span class="codeph"> 動非表</span> 示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

（オプション）

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`

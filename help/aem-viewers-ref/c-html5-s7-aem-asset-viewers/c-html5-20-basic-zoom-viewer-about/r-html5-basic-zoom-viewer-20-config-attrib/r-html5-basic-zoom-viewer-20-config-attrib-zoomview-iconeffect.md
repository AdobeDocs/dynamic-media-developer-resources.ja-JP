---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,User
exl-id: faec00b3-b981-4831-bc97-dff442389133
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態で、画像の操作に使用できるアクションがある場合に、IconEffectが画像の上部に表示されるようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffectの表示および再表示の最大回数を指定します。 値<span class="codeph"> -1</span>は、アイコンが常に無限に再表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p>表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p>IconEffectが完全に表示された状態を、自動的に非表示にするまでの秒数を設定します。 つまり、フェードインアニメーションが完了してから、フェードアウトアニメーションが開始するまでの時間です。 <span class="codeph"> 0</span>に設定すると、自動非表示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

（オプション）

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`

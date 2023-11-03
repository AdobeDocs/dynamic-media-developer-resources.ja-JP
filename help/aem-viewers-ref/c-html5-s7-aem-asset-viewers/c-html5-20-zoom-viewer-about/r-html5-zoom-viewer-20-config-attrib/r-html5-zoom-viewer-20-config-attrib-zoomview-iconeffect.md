---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 59d71d3b-706f-4f77-8e75-e24c5654f6e3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`フェード`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> を有効にします。 <span class="codeph"> iconeffect</span> ：画像がリセット状態で、画像を操作するための使用可能なアクションを示す場合に、画像の上部に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> カウント</span></span> </p> </td> 
   <td colname="col2"> <p> 最大回数を指定します。 <span class="codeph"> iconeffect</span> が表示され、再度表示されます。 値： <span class="codeph"> -1</span> は、アイコンが無期限に常に再表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> フェード</span></span> </p> </td> 
   <td colname="col2"> <p>表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>秒数を設定します。 <span class="codeph"> iconeffect</span> は、自動的に非表示になる前は完全に表示されたままになります。 つまり、フェードインアニメーションが完了してから、フェードアウトアニメーションが開始するまでの時間です。 設定 <span class="codeph"> 0</span> を指定すると、自動非表示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`

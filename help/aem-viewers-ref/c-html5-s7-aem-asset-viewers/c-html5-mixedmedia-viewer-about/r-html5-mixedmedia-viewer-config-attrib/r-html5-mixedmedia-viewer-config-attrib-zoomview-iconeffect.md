---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
topic: Dynamic media
uuid: 9eab6cb2-92a3-41d2-999a-254a7109d6b6
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---


# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`countfadeautoHide`*][, *``*][, *``*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態で、画像の操作に使用できるアクションがある場合に、<span class="codeph"> iconeffect</span>を画像の上部に表示できるようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> カウント</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> iconeffect</span>の表示および再表示の最大回数を指定します。 <span class="codeph"> -1</span>の値は、アイコンが無限に再表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> iconeffect</span>が完全に表示され、自動非表示になるまでの秒数を設定します。 つまり、フェードインアニメーションが完了してからフェードアウトアニメーション開始までの時間を指定します。 <span class="codeph"> 0</span>を設定すると、自動非表示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`

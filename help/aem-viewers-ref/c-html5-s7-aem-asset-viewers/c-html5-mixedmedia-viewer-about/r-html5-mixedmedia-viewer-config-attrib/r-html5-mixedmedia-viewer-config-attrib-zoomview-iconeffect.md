---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,User
exl-id: 40b7887d-d525-4816-8c72-9ef8f5948de3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態で、画像の操作に使用できるアクションがある場合、 <span class="codeph"> iconeffect</span>が画像の上部に表示されるようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> カウント</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> iconeffect</span>が表示され、再び表示される最大回数を指定します。 値<span class="codeph"> -1</span>は、アイコンが常に無限に再表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> iconeffect</span>が完全に表示されたままになる秒数を設定します。この秒数を超えると、自動的に非表示になります。 つまり、フェードインアニメーションが完了してから、フェードアウトアニメーションが開始するまでの時間です。 <span class="codeph"> 0</span>に設定すると、自動非表示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`

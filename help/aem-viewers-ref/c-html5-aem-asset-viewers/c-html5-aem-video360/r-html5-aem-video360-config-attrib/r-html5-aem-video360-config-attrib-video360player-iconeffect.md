---
description: ビデオ360ビューアの設定属性。
solution: Experience Manager
title: Video360Player.iconeffect
feature: Dynamic Media Classic，ビューア，SDK/API,360 VRビデオ
role: Developer,Business Practitioner
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 7%

---

# Video360Player.iconeffect{#video-player-iconeffect}

ビデオ360ビューアの設定属性。

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> ビデオが一時停止状態の場合に、ビデオの上にIconEffectを表示できるようにします。 一部のデバイスでは、ネイティブのコントロールが使用されます。 その場合、 <span class="codeph"> iconeffect</span>修飾子は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> カウント</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectの表示および再表示の最大回数を指定します。 値<span class="codeph"> -1</span>は、アイコンが無期限に再び表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p> 表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectが完全に表示されたまま、自動非表示になるまでの秒数を設定します。 つまり、フェードインアニメーションが完了してから、フェードアウトアニメーションが開始するまでの時間です。 <span class="codeph"> 0</span>に設定すると、自動非表示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`

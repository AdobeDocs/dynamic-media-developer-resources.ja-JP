---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 4%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

インタラクティブビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *`countfadeautoHide`*][, *``*][, *``*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> ビデオが一時停止状態の場合に、ビデオの上部にIconEffectを表示するようにします。 一部のデバイスでは、ネイティブのコントロールが使用されます。 このような場合、<span class="codeph"> iconeffect</span>修飾子は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> カウント</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectの表示および再表示の最大回数を指定します。 <span class="codeph"> -1</span>の値は、アイコンが無限に再表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p> 表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectが完全に表示され、自動非表示になるまでの秒数を設定します。 つまり、フェードインアニメーションが完了してから、フェードアウトアニメーション開始までの時間を指定します。 <span class="codeph"> 0</span>に設定すると、自動非表示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`

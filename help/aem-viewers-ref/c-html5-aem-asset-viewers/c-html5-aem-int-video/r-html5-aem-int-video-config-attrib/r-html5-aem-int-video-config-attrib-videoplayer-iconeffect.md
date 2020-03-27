---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: a403d44d-d5b5-4d09-876e-39146585704f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

インタラクティブビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *`countfadeautoHide`*][, *``*][, *``*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> ビデオが一時停止状態の場合に、ビデオの上部にIconEffectを表示することを有効にします。 一部のデバイスでは、ネイティブのコントロールが使用されます。 この場合、iconeffect修飾子は <span class="codeph"> 無視され</span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> カウント</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectの表示と再表示の最大回数を指定します。 値が —1の場合、ア <span class="codeph"> イコンは</span> 無期限に再表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p> 表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectが完全に表示された状態で、自動非表示になるまでの秒数を設定します。 つまり、フェードインアニメーションが完了してから、フェードアウトアニメーションが開始するまでの時間です。 自動非表示の動 <span class="codeph"> 作を無効</span> にするには、0に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`

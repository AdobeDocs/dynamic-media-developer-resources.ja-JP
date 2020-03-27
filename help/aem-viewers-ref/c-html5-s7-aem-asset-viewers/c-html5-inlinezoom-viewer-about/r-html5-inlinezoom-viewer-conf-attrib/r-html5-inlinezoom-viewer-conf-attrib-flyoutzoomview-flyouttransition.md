---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic media
uuid: 0b94956d-9ee6-409e-9b52-29c888932a0e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`showtimeshowdelayhidetimehidedelay`*[, *``*[, *``*[, *``*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|fade </span></span> </p> </td> 
   <td colname="col2"> <p> フライアウトビューの表示/非表示時に適用する効果のタイプを指定します。 なしの場 <span class="codeph"> 合、フラ </span>イアウト画像はアクティブ化され、準備が整ったらすぐに表示されます。 <span class="codeph"> slide </span> は、スライドアニメーションを左から右の方向に再生します。fadeは、フ <span class="codeph"></span> ライアウト画像にアルファトランジションを適用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ショー </span> 時間 </span> </p> </td> 
   <td colname="col2"> <p> アニメーションの表示が完了するまでの秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span></span> </p> </td> 
   <td colname="col2"> <p> アニメーションの表示を開始するユーザアクションと、アニメーションの表示を開始する操作の間の遅延（秒単位）です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 隠れ </span> 時 </span> </p> </td> 
   <td colname="col2"> <p> 非表示アニメーションの完了に要する秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span></span> </p> </td> 
   <td colname="col2"> <p> アニメーションの非表示を開始するユーザアクションと、アニメーション自体の非表示の開始との間の遅延（秒単位）です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`

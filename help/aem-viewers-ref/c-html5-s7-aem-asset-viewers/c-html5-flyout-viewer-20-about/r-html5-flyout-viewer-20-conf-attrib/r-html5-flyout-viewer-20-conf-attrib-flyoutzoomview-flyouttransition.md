---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic media
uuid: f1a9f2bc-9a13-4980-9241-e835a0aadd2c
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

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`

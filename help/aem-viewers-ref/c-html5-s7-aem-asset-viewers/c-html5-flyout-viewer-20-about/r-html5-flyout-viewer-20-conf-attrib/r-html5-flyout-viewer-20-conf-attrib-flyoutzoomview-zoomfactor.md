---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> フライアウト ビューのイメージの倍率を、メイン ビューを基準にして指定します。 1.0</span> 以上の整数値または浮動小数点値 <span class="codeph"> ある必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> ハイライトがアクティブな状態でメイン ビューをクリックまたはタップすると、アクセスできるオプションのサブ要因を指定できます。 2 回目にクリックまたはタップすると、プライマリズーム率に戻ります。 値が <span class="codeph">-1</span> の場合、2 次ズーム倍率は無効になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>アップスケ <span class="codeph"><span class="varname"> ル </span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントによる小さい画像の処理方法を指定します。 </p> <p><span class="codeph">1 に設定すると </span> コンポーネントはメイン画像を拡大/縮小して、メインビュー内に収まるようにします。 また、設定済みのフライアウトウィンドウ領域を完全に満たすように、ズーム画像を拡大します。 </p> <p><span class="codeph"> 0</span> に設定すると、小さな画像は元の解像度で表示され、メイン表示領域とフライアウトウィンドウの中央に表示されます。 メインビューの <span class="codeph"> s7flyoutzoomview クラスおよびフライアウトウィンドウの s7flyoutzoom</span>CSS クラスの背景や類似の CSS プロパティを使用して </span> 画像の周囲に表示され <span class="codeph"> 追加の空白を設定することができます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`

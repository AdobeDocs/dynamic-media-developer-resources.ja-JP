---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> フライアウト ビューのイメージの倍率を、メイン ビューを基準にして指定します。 1.0<span class="codeph"> 以上の整数値または浮動小数点値 </span> ある必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> ハイライトがアクティブな状態でメイン ビューをクリックまたはタップすると、アクセスできるオプションのサブ要因を指定できます。 2 回目にクリックまたはタップすると、プライマリズーム率に戻ります。 値が <span class="codeph">-1</span> の場合、2 次ズーム倍率は無効になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>アップスケ <span class="codeph"><span class="varname"> ル </span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントによる小さい画像の処理方法を指定します。 </p> <p><span class="codeph">1 に設定すると </span> コンポーネントはメイン画像を拡大/縮小して、メインビュー内に収まるようにします。 また、設定済みのフライアウトウィンドウ領域を完全に満たすように、ズーム画像を拡大します。 </p> <p><span class="codeph"> 0</span> に設定すると、小さな画像は元の解像度で表示され、メイン表示領域とフライアウトウィンドウの中央に表示されます。 メインビューの <span class="codeph"> s7flyoutzoomview の背景または類似の CSS プロパティとメインビューの s7flyoutzoom</span> およびフライアウトウィンドウの <span class="codeph"> s7flyoutzoom</span>CSS クラスを使用して、画像の周囲に追加の空白を設定できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

オプション。

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`

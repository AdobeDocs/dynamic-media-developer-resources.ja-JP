---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
feature: Dynamic Media Classic，ビューア，SDK/API，フライアウト
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 2%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondaryFactupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> メインビューを基準とした、フライアウトビューの画像の倍率を指定します。<span class="codeph"> 1.0</span>以上の整数または浮動小数点値を指定する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> オプションでセカンダリ係数を指定できます。これには、ハイライトがアクティブなときにメインビューをクリックまたはタップしてアクセスできます。 2回目にクリックまたはタップすると、プライマリズーム率に戻ります。 値<span class="codeph"> -1</span>を指定すると、セカンダリズーム率が無効になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントでの小さな画像の処理方法を指定します。 </p> <p><span class="codeph"> 1</span>に設定すると、メイン画像がメインビュー内に収まるように拡大されます。 また、ズーム画像が拡大され、設定したフライアウトウィンドウ領域が完全に埋まります。 </p> <p><span class="codeph"> 0</span>に設定すると、小さい画像が元の解像度で表示され、メインビュー領域とフライアウトウィンドウ内で中央に表示されます。 メインビューとフライアウトウィンドウのそれぞれで、 <span class="codeph"> s7flyoutzoomview</span>および<span class="codeph"> s7flyoutzoom</span> CSSクラスのbackgroundまたは類似のCSSプロパティを使用して、画像の周囲に余白を設定できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`

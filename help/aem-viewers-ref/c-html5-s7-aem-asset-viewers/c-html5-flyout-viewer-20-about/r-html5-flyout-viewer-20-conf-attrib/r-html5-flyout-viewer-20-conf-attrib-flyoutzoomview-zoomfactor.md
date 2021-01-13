---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondaryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> メイン画像を基準にした、フライアウト表示の表示の倍率を指定します。<span class="codeph"> 1.0</span>以上の整数または浮動小数点値です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> オプションでセカンダリ要因を指定できます。これにアクセスするには、ハイライトがアクティブなときにメイン表示をクリックまたはタップします。 もう一度タップすると、プライマリズーム率に戻ります。 値<span class="codeph"> -1</span>はセカンダリズーム率を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントでの小さい画像の処理方法を指定します。 </p> <p><span class="codeph"> 1</span>に設定した場合、メイン表示がメイン画像内に収まるようにメイン画像が拡大されます。 また、ズーム画像が拡大され、設定したフライアウトウィンドウ領域全体に表示されます。 </p> <p><span class="codeph"> 0</span>に設定した場合、小さい画像は元の解像度で表示され、メイン表示領域とフライアウトウィンドウ内の中央に表示されます。 メイン表示ーとフライアウトウィンドウのそれぞれで、<span class="codeph"> s7flyoutzoomview</span>および<span class="codeph"> s7flyoutzoom</span> CSSクラスのbackgroundまたは同様のCSSプロパティを使用して、画像の周囲に余白を表示するように設定できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`

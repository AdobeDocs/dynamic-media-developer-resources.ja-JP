---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactorsecondaryFactorupscale`*[,[ *``*][, *``*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 主 <span class="varname"> 要因</span></span> </p> </td> 
   <td colname="col2"> <p> メインビューを基準とした、フライアウトビューの画像の倍率を指定します。1.0以上の整数または浮動小数点値 <span class="codeph"> である必要</span> があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 二 <span class="varname"> 次因子</span></span> </p> </td> 
   <td colname="col2"> <p> オプションでセカンダリ要素を指定できます。これにアクセスするには、ハイライトがアクティブなときにメインビューをクリックまたはタップします。 もう一度クリックまたはタップすると、プライマリズーム率に戻ります。 -1を指定すると、セ <span class="codeph"> カンダリズーム</span> 率が無効になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高級な</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントでの小さい画像の処理方法を指定します。 </p> <p>1に設定すると、メ <span class="codeph"> イン</span> 画像がメインビュー内に収まるように拡大されます。 また、ズーム画像が拡大され、設定されたフライアウトウィンドウ領域が完全に埋められます。 </p> <p>0に設定すると <span class="codeph"></span> 、小さい画像は元の解像度で表示され、メインビュー領域とフライアウトウィンドウ内の中央に表示されます。 メインビューとフライアウトウィンドウのそれぞれで、 <span class="codeph"> s7flyoutzoomview</span><span class="codeph"></span> CSSクラスのbackgroundまたは類似のCSSプロパティを使用して、画像の周囲に余分な空白を表示するように設定できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`

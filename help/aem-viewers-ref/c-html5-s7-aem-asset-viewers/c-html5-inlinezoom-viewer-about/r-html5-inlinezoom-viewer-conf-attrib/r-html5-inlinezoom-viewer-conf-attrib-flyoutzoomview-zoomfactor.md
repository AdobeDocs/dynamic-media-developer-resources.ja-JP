---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 8c4e6bf8-0238-470b-9fbe-262eb17f8f3b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
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
   <td colname="col2"> <p>コンポーネントでの小さい画像の処理方法を指定します。 </p> <p><span class="codeph"> 1</span>に設定した場合、メイン表示がメイン画像内に収まるようにメイン画像が拡大されます。 また、ズーム画像が拡大され、設定したフライアウトウィンドウ領域全体に表示されます。 </p> <p><span class="codeph"> 0</span>に設定した場合、小さい画像は元の解像度で表示され、メイン表示領域とフライアウトウィンドウ内の中央に表示されます。 メイン表示とフライアウトウィンドウのそれぞれで、<span class="codeph"> s7flyoutzoomview</span>および<span class="codeph"> s7flyoutzoom</span> CSSクラスのbackgroundまたは同様のCSSプロパティを使用して、画像の周囲に余白を設定できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`

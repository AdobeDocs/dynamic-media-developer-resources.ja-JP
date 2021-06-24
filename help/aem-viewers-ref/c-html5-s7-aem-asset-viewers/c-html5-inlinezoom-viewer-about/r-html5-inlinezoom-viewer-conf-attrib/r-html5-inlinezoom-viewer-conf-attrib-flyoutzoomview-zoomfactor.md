---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,Business Practitioner
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '184'
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
   <td colname="col2"> <p>コンポーネントでの小さな画像の処理方法を指定します。 </p> <p><span class="codeph"> 1</span>に設定すると、メイン画像がメインビュー内に収まるように拡大されます。 また、ズーム画像が拡大され、設定したフライアウトウィンドウ領域が完全に埋まります。 </p> <p><span class="codeph"> 0</span>に設定すると、小さい画像が元の解像度で表示され、メインビュー領域とフライアウトウィンドウ内で中央に表示されます。 メインビューとフライアウトウィンドウのそれぞれで、 <span class="codeph"> s7flyoutzoomview</span>および<span class="codeph"> s7flyoutzoom</span> CSSクラスのbackgroundまたは類似のCSSプロパティを使用して、画像の周囲に余分な空白を設定できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`

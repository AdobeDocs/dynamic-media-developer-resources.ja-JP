---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`アップスケール`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> メインビューを基準にした、フライアウトビューの画像の倍率を指定します。整数または浮動小数点値である必要があります <span class="codeph"> 1.0</span> 以上 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> オプションでセカンダリ係数を指定できます。この係数にアクセスするには、ハイライトがアクティブなときにメインビューをクリックまたはタップします。 2 回目にクリックまたはタップすると、プライマリズーム率に戻ります。 値： <span class="codeph"> -1</span> セカンダリズーム率を無効にします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> アップスケール</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントでの小さな画像の処理方法を指定します。 </p> <p>次に設定した場合： <span class="codeph"> 1</span> メイン画像は、メインビュー内に収まるように拡大されます。 また、ズーム画像が拡大され、設定されたフライアウトウィンドウ領域が完全に埋められます。 </p> <p>次に設定した場合： <span class="codeph"> 0</span>に設定すると、小さな画像は元の解像度で表示され、メインビュー領域とフライアウトウィンドウ内で中央に表示されます。 画像の周囲に表示される余分な空白を、背景または類似の CSS プロパティ ( <span class="codeph"> s7flyoutzoomview</span> および <span class="codeph"> s7flyoutzoom</span> メインビューとフライアウトウィンドウのそれぞれの CSS クラス。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`

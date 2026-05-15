---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
TQID: 'https://experienceleague.adobe.com/Zp4VYoGBfivwXRZQ7dmtouoy2qFMZePQKDrocHaBPXk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> メインビューに対するフライアウトビューの画像倍率を指定します。 整数値または浮動小数点値<span class="codeph"> 1.0</span>以上である必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> ハイライトがアクティブな状態でメインビューをクリックまたはタップすることで、オプションの二次要素を指定できます。 2回目をクリックまたはタップすると、メインのズーム係数に戻ります。 値<span class="codeph"> -1</span>を指定すると、第2 ズーム係数が無効になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> アップスケール </span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントが小さな画像をどのように処理するかを指定します。 </p> <p><span class="codeph"> 1</span>に設定すると、コンポーネントはメイン画像をアップスケールして、メインビュー内に収まるようにします。 また、設定したフライアウトウィンドウ領域を完全に塗りつぶすように、ズーム画像をアップスケールします。 </p> <p><span class="codeph"> 0</span>に設定すると、小さな画像が元の解像度で表示され、メインビュー領域とフライアウトウィンドウ内に中央に表示されます。 メインビューとフライアウトウィンドウで、<span class="codeph"> s7flyoutzoomview</span>と<span class="codeph"> s7flyoutzoom</span> CSS クラスの背景または類似のCSS プロパティを使用して、画像の周囲に表示される余白を設定できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`

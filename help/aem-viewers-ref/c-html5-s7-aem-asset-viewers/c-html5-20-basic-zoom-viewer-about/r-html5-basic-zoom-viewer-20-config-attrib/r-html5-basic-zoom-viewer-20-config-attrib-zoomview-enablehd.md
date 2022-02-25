---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 2%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`番号`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> 次の場合に最適化を有効、制限、無効にします。 <span class="codeph"> devicePixelRatio</span> 次よりも大きい <span class="codeph"> 1</span>:iPhone4 などの高密度ディスプレイを持つデバイス。 有効にすると、デバイスのピクセル比がのみであるかのように、コンポーネントが IS イメージリクエストのサイズを制限します。 <span class="codeph"> 1</span> これにより、帯域幅が削減されます。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 数値</span> </span> </p> </td> 
   <td colname="col2"> <p> limit 設定を使用すると、指定した制限値までの高ピクセル密度のみが有効になります。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

（オプション）

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

この設定属性をビューアで使用し、ビューアのサイズが 1000 x 1000 の場合、次のような結果が期待されます。

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>設定変数が </p> </th> 
   <th colname="col2" class="entry"> <p>結果 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> いつも</span> </p> </td> 
   <td colname="col2"> <p>画面/デバイスのピクセル密度は常に考慮されます。</p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>画面のピクセル密度= 1 の場合、要求される画像は 1000 x 1000 です。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>画面のピクセル密度= 1.5 の場合、要求される画像は 1500 x 1500 です。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>画面のピクセル密度= 2 の場合、要求される画像は 2000 x 2000 です。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 決してない</span> </p> </td> 
   <td colname="col2"> <p>常にピクセル密度 1 を使用し、デバイスの HD 機能は無視されます。 したがって、リクエストされるイメージは常に 1000 x 1000 です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 制限&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>デバイスのピクセル密度が要求され、提供されるのは、結果の画像が指定された制限を下回る場合のみです。 </p> <p>制限値は、幅または高さの寸法に適用されます。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>制限値が 1600 で、ピクセル密度が 1.5 の場合、1500 x 1500 の画像が提供されます。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>制限値が 1600 で、ピクセル密度が 2 の場合、2000 x 2000 の画像は制限を超えるので、1000 x 1000 の画像が提供されます。 </p> </li> 
     </ul> </p> <p> <b>ベストプラクティス</b>:この制限数は、画像の最大サイズに関する会社の設定と連携する必要があります。 したがって、制限値を会社の最大画像サイズ設定と等しく設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 2%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`番号`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> devicePixelRatio</span>が<span class="codeph"> 1</span>より大きいデバイス（iPhone4など高密度ディスプレイを使用するデバイス）の最適化の有効化、制限または無効化を行います。 有効にすると、デバイスのピクセル比が<span class="codeph"> 1</span>の場合と同じように、コンポーネントでISイメージリクエストのサイズが制限され、帯域幅が削減されます。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 数値</span> </span> </p> </td> 
   <td colname="col2"> <p> limit設定を使用すると、指定した制限値までの高ピクセル密度が有効になります。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

（オプション）

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

この設定属性をビューアで使用し、ビューアのサイズが1000 x 1000の場合に期待される結果は次のとおりです。

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
   <td colname="col2"> <p>画面/デバイスのピクセル密度が常に考慮されます。 </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>画面のピクセル密度= 1の場合、要求される画像は1000 x 1000です。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>画面のピクセル密度= 1.5の場合、要求される画像は1500 x 1500です。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>画面のピクセル密度= 2の場合、要求される画像は2000 x 2000です。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 決してない</span> </p> </td> 
   <td colname="col2"> <p>常にピクセル密度1を使用し、デバイスのHD機能を無視します。 したがって、要求されるイメージは常に1000 x 1000です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>デバイスのピクセル密度は、結果の画像が指定された制限を下回る場合にのみ要求され、提供されます。 </p> <p>制限値は、幅または高さの寸法に適用されます。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>制限値が1600で、ピクセル密度が1.5の場合は、1500 x 1500の画像が提供されます。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>制限値が1600で、ピクセル密度が2の場合は、2000 x 2000の画像が制限を超えるので、1000 x 1000の画像が提供されます。 </p> </li> 
     </ul> </p> <p> <b>ベストプラクティス</b>:この制限値は、画像の最大サイズに関する会社設定と組み合わせて使用する必要があります。したがって、制限値を会社の最大画像サイズ設定と等しく設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

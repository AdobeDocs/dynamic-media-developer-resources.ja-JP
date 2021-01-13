---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
topic: Dynamic media
uuid: 1ee3789d-a3eb-42f7-a0f4-71f62a54cab9
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`番号`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> devicePixelRatio</span>が<span class="codeph"> 1</span>より大きいデバイス（iPhone4など高密度ディスプレイのデバイス）の最適化の有効化、制限または無効化を行います。 有効にすると、デバイスのピクセル率が<span class="codeph"> 1</span>のみであるかのようにコンポーネントでIS画像リクエストのサイズが制限され、帯域幅が減少します。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> number</span> </span> </p> </td> 
   <td colname="col2"> <p> limit設定を使用すると、指定した制限値までの高ピクセル密度が有効になります。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

（オプション）

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

ビューアでこの設定属性を使用し、ビューアサイズが1000 x 1000の場合、次のような結果が予測されます。

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
   <td colname="col2"> <p>ピクセル密度は常に1を使用し、デバイスのHD機能は無視されます。 したがって、要求される画像は常に1000 x 1000です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>デバイスのピクセル密度が要求され、提供されるのは、結果の画像が指定された制限を下回る場合のみです。 </p> <p>制限値は、幅または高さのどちらかに適用されます。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>制限値が1600で、ピクセル密度が1.5の場合、1500 x 1500の画像が提供されます。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>制限値が1600で、ピクセル密度が2の場合、1000 x 1000の画像が提供されます。これは、2000 x 2000の画像が制限を超えているからです。 </p> </li> 
     </ul> </p> <p> <b>ベストプラクティス</b>:この制限値は、画像の最大サイズに対する会社設定と組み合わせて使用する必要があります。したがって、制限値は、会社の最大画像サイズ設定と同じに設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>


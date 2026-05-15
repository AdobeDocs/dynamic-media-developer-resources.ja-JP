---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
TQID: 'https://experienceleague.adobe.com/IxWBmkKfrj-lDgQXXglzq2Q19e8YoApJRzwT8P-L4a0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 306
ht-degree: 1%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`number`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">は常に|決して|制限</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> devicePixelRatio</span>が<span class="codeph"> 1</span>より大きいデバイス、つまりiPhone4などの高密度ディスプレイを持つデバイスの最適化を有効、制限、または無効にします。 アクティブな場合、コンポーネントは、デバイスのピクセル比が<span class="codeph"> 1</span>のみであるかのようにIS画像要求のサイズを制限し、その方法で帯域幅を削減します。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> number</span> </span> </p> </td> 
   <td colname="col2"> <p> 制限の設定を使用する場合、コンポーネントは指定された制限までしか高いピクセル密度を有効にしません。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-50bcd15223174bb79ce08b31ea03d682}

オプション。

## 初期設定 {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## 例 {#section-96e69b70365f461dae4399e49044ea2f}

ビューアでこの設定属性を使用し、ビューアサイズが1000 x 1000の場合に想定される結果は次のとおりです。

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>set変数が </p> </th> 
   <th colname="col2" class="entry"> <p>結果 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">は常に</span> </p> </td> 
   <td colname="col2"> <p>画面/デバイスのピクセル密度は常に考慮されます。</p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>画面のピクセル密度= 1の場合、要求された画像は1000 x 1000です。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>画面のピクセル密度= 1.5の場合、要求された画像は1500 x 1500です。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>画面のピクセル密度= 2の場合、要求された画像は2000 x 2000です。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> never</span> </p> </td> 
   <td colname="col2"> <p>ピクセル密度は常に1で、デバイスのHD機能は無視されます。 したがって、要求された画像は常に1000 x 1000になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">制限&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>デバイスのピクセル密度が要求され、結果の画像が指定された制限を下回る場合にのみ提供されます。 </p> <p>制限番号は、幅または高さの寸法のいずれかに適用されます。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>制限番号が1600、ピクセル密度が1.5の場合、1500 x 1500の画像が提供されます。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>制限番号が1600、ピクセル密度が2の場合、2000 x 2000の画像が制限を超えているため、1000 x 1000の画像が提供されます。 </p> </li> 
     </ul> </p> <p> <b> ベストプラクティス </b>：最大サイズの画像を得るには、会社の設定で制限の数を指定する必要があります。 したがって、会社の最大画像サイズ設定と同じ制限サイズに制限を設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

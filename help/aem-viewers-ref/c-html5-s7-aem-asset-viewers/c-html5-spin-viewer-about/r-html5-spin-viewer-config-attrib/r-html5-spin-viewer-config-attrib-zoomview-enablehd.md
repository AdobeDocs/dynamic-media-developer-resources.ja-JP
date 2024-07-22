---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: fd81cd48-9990-4659-a52c-7abdbc95a0e3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 1%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *` 数値 `*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> devicePixelRatio</span> が <span class="codeph"> 1</span> より大きいデバ <span class="codeph"> ス、つまりiPhone4 などの高密度ディスプレイを使用するデバイスの最適化を有効、制限、または無効にします。 アクティブの場合、デバイスのピクセル比が <span class="codeph"> 1 しかないかのようにコンポーネントが IS 画像リクエストのサイズを制限し </span> 帯域幅が削減されます。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数 </span></span> </p> </td> 
   <td colname="col2"> <p> リミット設定を使用する場合、コンポーネントは指定されたリミットまでの高画素密度のみを有効にします。 </p> <p>以下の例を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`limit,1500`

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

以下は、ビューアでこの設定属性を使用し、ビューアサイズが 1000 x 1000 の場合に期待される結果です。

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>設定変数がに等しい場合 </p> </th> 
   <th colname="col2" class="entry"> <p>結果 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> つも </span> </p> </td> 
   <td colname="col2"> <p>画面/デバイスのピクセル密度は常に考慮されます。 </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>画面のピクセル密度= 1 の場合、リクエストされた画像は 1000 x 1000 です。 </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>画面のピクセル密度= 1.5 の場合、リクエストされた画像は 1500 x 1500 です。 </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>画面のピクセル密度= 2 の場合、リクエストされた画像は 2000 x 2000 です。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>決して <span class="codeph"> らない </span> </p> </td> 
   <td colname="col2"> <p>常に 1 のピクセル密度を使用し、デバイスの HD 機能を無視します。 したがって、リクエストされた画像は常に 1000 x 1000 になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>デバイスピクセル密度は、結果の画像が指定された制限を下回る場合にのみ要求され、提供されます。 </p> <p>制限数は、幅または高さの寸法に適用されます。 </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>制限数が 1600 で、ピクセル密度が 1.5 の場合、1500 x 1500 の画像が提供されます。 </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>制限数が 1600 で、ピクセル密度が 2 の場合、2000 x 2000 の画像が制限を超えているので、1000 x 1000 の画像が提供されます。 </p> </li> 
     </ul> </p> <p><b> ベストプラクティス </b>：制限数は、会社の設定と一致して最大サイズの画像にする必要があります。 そのため、制限数は会社の最大画像サイズ設定と同じ数に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

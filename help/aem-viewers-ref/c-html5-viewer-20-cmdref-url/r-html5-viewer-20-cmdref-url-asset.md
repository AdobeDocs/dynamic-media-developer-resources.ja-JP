---
title: asset
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: edcd18b6-5292-44da-80be-b7f75ee4c48e
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---

# asset{#asset}

すべてのビューアに共通のパラメーター。

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId </span> </span> </p> </td> 
   <td colname="col2"> <p> 単一のビデオまたはアダプティブビデオセットのアセット ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

このパラメーターを使用しない限り、こ `video` プロパティは必須です。 詳しくは、「ビデオ」の [ 外部ビデオのサポート ](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) または「ビデオ 360」の [ 外部ビデオのサポート ](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) を参照してください。

または

` asset= *` 画像 `*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 画像 </span> </span> </p> </td> 
   <td colname="col2"> <p> 単一の画像またはカルーセルセットを指定します。 画像名またはカルーセルセット名に存在する安全でない文字に、ダブル HTTP エンコーディングを適用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

または

` asset= *`image`* | *`imageList`* | *`imageListWithModifiers`* | *`multiDimensionalSpinSet`* [%3F *`modifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 画像 </span> </span> </p> </td> 
   <td colname="col2"> <p> 単一の画像を指定します。 画像名に存在する安全でない文字に、ダブル HTTP エンコーディングを適用します。 </p> <p>または、画像セットへの参照を指定します。 ビューアは、req=set IS <span class="codeph"> リクエスト </span> 使用して、サーバーから画像セットを取得します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList </span> </span> </p> </td> 
   <td colname="col2"> <p> コンマで区切られた項目またはフレームの並べ替えられたシーケンスで構成される、明示的な画像セットを指定します。 </p> <p> <p>メモ：この機能はAdobe Dynamic Media Classicでサポートされます。Adobe Experience Manager Assetsではサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers </span> </span> </p> </td> 
   <td colname="col2"> <p> 各フレームに独自の画像サービング修飾子がある明示的な画像セットを指定します。 この場合、フレームのリストはかっこで囲まれます。 フレーム固有の画像サービング修飾子に存在する任意のコンマに、ダブル HTTP エンコーディングを適用してください。 </p> <p> <p>メモ：この機能はAdobe Dynamic Media Classicでサポートされます。Adobe Experience Manager Assetsではサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet </span> </span> </p> </td> 
   <td colname="col2"> <p>次の構文を使用して、明示的な多次元スピンセットを指定します。 </p> <p> <span class="codeph"> （（<span class="varname"> horizontalSpinSet </span>） [,（<span class="varname"> horizontalSpinSet </span>） ]） </span> </p> <p> <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> は、指定した水平軸のフレームのコンマ区切りリストです。 <span class="codeph"><span class="varname"></span> すべての horizontalSpinSet</span> フレーム数は同じにする必要があります。 </p> <p> <p>メモ：この機能はAdobe Dynamic Media Classicでサポートされます。Adobe Experience Manager Assetsではサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 修飾子 </span> </span> </p> </td> 
   <td colname="col2"> <p> 画像サービング コマンド；<span class="codeph"> &amp; </span> および <span class="codeph"> = </span><span class="codeph"> 区切り記号は、それぞれ %26 </span> および <span class="codeph"> %3D </span> として HTTP エンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

または

` asset=( *`mediaSet`* | ( *`video`*; *`swatchId`* | *`image`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;( *`video`*; *`swatchId`* | *`image`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;] [%3F *`modifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet </span> </span> </p> </td> 
   <td colname="col2"> <p> メディアセットへの参照を指定します。 ビューアは、req=set IS リクエストを使用して、サーバーからメディアセットを取得します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> video </span> </span> </p> </td> 
   <td colname="col2"> <p> 単一のビデオまたはアダプティブビデオセット。 </p> <p> <p>メモ：この機能はAdobe Dynamic Media Classicでサポートされます。Adobe Experience Manager Assetsではサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 画像 </span> </span> </p> </td> 
   <td colname="col2"> <p> 単一の画像。 </p> <p> <p>メモ：この機能はAdobe Dynamic Media Classicでサポートされます。Adobe Experience Manager Assetsではサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId </span> </span> </p> </td> 
   <td colname="col2"> <p> スウォッチセット。 </p> <p> <p>メモ：この機能はAdobe Dynamic Media Classicでサポートされます。Adobe Experience Manager Assetsではサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId </span> </span> </p> </td> 
   <td colname="col2"> <p>スウォッチ画像。 </p> <p> <p>メモ：この機能はAdobe Dynamic Media Classicでサポートされます。Adobe Experience Manager Assetsではサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID </span> </span> </p> </td> 
   <td colname="col2"> <p> メディアセットの項目タイプ識別子は、次のいずれかになります。 </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image </span> </p> <p>単一の画像の場合。 </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset </span> </p> <p>ネストされたスウォッチセットの場合。 </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> spin </span> </p> <p>スピンセットの場合。 </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> video </span> </p> <p>単一のビデオの場合。 </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set </span> </p> <p>（アダプティブビデオセットの場合） </p> </li> 
     </ul> </p> <p> <p>メモ：この機能はAdobe Dynamic Media Classicでサポートされます。Adobe Experience Manager Assetsではサポートされません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 修飾子 </span> </span> </p> </td> 
   <td colname="col2"> <p> 画像サービング コマンド；<span class="codeph"> &amp; </span> および <span class="codeph"> = </span><span class="codeph"> 区切り記号は、それぞれ %26 </span> および <span class="codeph"> %3D </span> として HTTP エンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>IR （画像レンダリング）または UGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

必須。

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

なし

## 例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

単一アセット参照：

```
asset=Scene7SharedAssets/Backpack_B
```

または

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

または

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

または

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

または

```
asset=Viewers/space_station_360-AVS
```

カタログで定義される画像セットへの単一の参照：

```
asset=Viewers/Pluralist
```

明示的な画像セット：

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

フレーム固有の画像サービング修飾子を持つ明示的な画像セット：

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

カタログで定義されるスピンセットへの単一の参照：

```
asset=Scene7SharedAssets/SpinSet-Sample
```

明示的スピンセット：

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

明示的な多次元スピンセット：

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

単一の混在メディアセットの参照：

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

明示的混在メディアセット：

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

セット内のすべての画像に追加されたシャープニング修飾子：

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```

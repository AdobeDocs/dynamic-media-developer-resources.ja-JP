---
title: asset
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: edcd18b6-5292-44da-80be-b7f75ee4c48e
TQID: 'https://experienceleague.adobe.com/EylLoY4VQMafn65jykpRSh99ZuybGh5bx-RVhmJnyTE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 562
ht-degree: 2%

---

# asset{#asset}

すべてのビューアに共通のパラメーター。

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId </span> </span> </p> </td> 
   <td colname="col2"> <p> 単一ビデオまたはアダプティブビデオセットのアセット ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

このプロパティは、`video` パラメーターを使用しない限り必須です。 ビデオの下の[外部ビデオサポート &#x200B;](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3)またはVideo360の下の[外部ビデオサポート &#x200B;](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760)を参照してください。

または

` asset= *`画像`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">画像</span> </span> </p> </td> 
   <td colname="col2"> <p> 単一の画像またはカルーセルセットを指定します。 画像名またはカルーセルセット名に存在する安全でない文字に対して、二重HTTP エンコーディングを適用します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

または

` asset= *`image`* | *`imageList`* | *`imageListWithModifiers`* | *`multiDimensionalSpinSet`* [%3F *`modifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">画像</span> </span> </p> </td> 
   <td colname="col2"> <p> 単一の画像を指定します。 画像名に存在する安全でない文字に対して、二重HTTP エンコーディングを適用します。 </p> <p>または、画像セットへの参照を指定します。 ビューアは、<span class="codeph"> req=set IS </span> リクエストを使用して、サーバーから画像セットを取得します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList </span> </span> </p> </td> 
   <td colname="col2"> <p> アイテムまたはフレームの並べ替えシーケンスで構成される明示的な画像セットをコンマで区切って指定します。 </p> <p> <p>注意：この機能はAdobe Dynamic Media Classicでサポートされており、Adobe Experience Manager Assetsではサポートされていません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers </span> </span> </p> </td> 
   <td colname="col2"> <p> 各フレームに独自の画像サービング修飾子がある明示的な画像セットを指定します。 この場合、フレームのリストは括弧で囲まれます。 フレーム固有の画像サービング修飾子に存在するコンマには、必ず二重HTTP エンコーディングを適用してください。 </p> <p> <p>注意：この機能はAdobe Dynamic Media Classicでサポートされており、Adobe Experience Manager Assetsではサポートされていません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet </span> </span> </p> </td> 
   <td colname="col2"> <p>次の構文を使用して、明示的な多次元スピンセットを指定します。 </p> <p> <pre><code>(( horizontalSpinSet )&lbrack;&lbrack;,( horizontalSpinSet )&rbrack;)</code></pre> </p> <p> ここで、<span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span>は、特定の水平軸のフレームのコンマ区切りリストです。 すべての<span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span>のフレーム数は同じである必要があります。 </p> <p> <p>注意：この機能はAdobe Dynamic Media Classicでサポートされており、Adobe Experience Manager Assetsではサポートされていません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">修飾子</span> </span> </p> </td> 
   <td colname="col2"> <p> 画像サービングコマンド。<span class="codeph">および</span>および<span class="codeph"> = </span>区切り記号はそれぞれ<span class="codeph"> %26 </span>および<span class="codeph"> %3D </span>としてHTTP エンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

または

` asset=( *`mediaSet`* | ( *`video`*; *`swatchId`* | *`image`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;( *`video`*; *`swatchId`* | *`image`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;] [%3F *`modifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet </span> </span> </p> </td> 
   <td colname="col2"> <p> メディアセットへの参照を指定します。 ビューアは、req=set IS リクエストを使用してサーバーからメディアセットを取得します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ビデオ </span> </span> </p> </td> 
   <td colname="col2"> <p> 単一ビデオまたはアダプティブビデオセット。 </p> <p> <p>注意：この機能はAdobe Dynamic Media Classicでサポートされており、Adobe Experience Manager Assetsではサポートされていません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">画像</span> </span> </p> </td> 
   <td colname="col2"> <p> 単一の画像： </p> <p> <p>注意：この機能はAdobe Dynamic Media Classicでサポートされており、Adobe Experience Manager Assetsではサポートされていません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId </span> </span> </p> </td> 
   <td colname="col2"> <p> スウォッチセット： </p> <p> <p>注意：この機能はAdobe Dynamic Media Classicでサポートされており、Adobe Experience Manager Assetsではサポートされていません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId </span> </span> </p> </td> 
   <td colname="col2"> <p>スウォッチ画像： </p> <p> <p>注意：この機能はAdobe Dynamic Media Classicでサポートされており、Adobe Experience Manager Assetsではサポートされていません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID </span> </span> </p> </td> 
   <td colname="col2"> <p> メディアセット項目タイプ識別子は、次のいずれかになります。 </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image </span> </p> <p>単一の画像の場合。 </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset </span> </p> <p>ネストされたスウォッチセットの場合。 </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> スピン </span> </p> <p>スピンセット用。 </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph">動画</span> </p> <p>単一のビデオの場合 </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set </span> </p> <p>組み合わせることから始めます。 </p> </li> 
     </ul> </p> <p> <p>注意：この機能はAdobe Dynamic Media Classicでサポートされており、Adobe Experience Manager Assetsではサポートされていません。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">修飾子</span> </span> </p> </td> 
   <td colname="col2"> <p> 画像サービングコマンド。<span class="codeph">および</span>および<span class="codeph"> = </span>区切り記号はそれぞれ<span class="codeph"> %26 </span>および<span class="codeph"> %3D </span>としてHTTP エンコードする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>IR （画像レンダリング）またはUGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

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

カタログで定義されている画像セットへの単一参照：

```
asset=Viewers/Pluralist
```

明示的な画像セット：

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

フレーム固有の画像サービング修飾子を使用した明示的な画像セット：

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

カタログで定義されているスピンセットへの単一参照：

```
asset=Scene7SharedAssets/SpinSet-Sample
```

明示的なスピンセット：

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

明示的な多次元スピンセット：

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

単一の混在メディアセット参照：

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

明示的な混在メディアセット：

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

シャープ修飾子がセット内のすべての画像に追加されました。

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```

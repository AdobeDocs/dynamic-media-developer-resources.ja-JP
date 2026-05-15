---
title: ホットスポットと画像マップ
description: ビューアは、AEM AssetsのDynamic Mediaでホットスポットを作成した場所に、メインビュー上にホットスポットアイコンをオンデマンドで表示します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
TQID: 'https://experienceleague.adobe.com/47IGGdIHBBuI5KUh6gKw-8imQCcM-BVAQkLPZhY5-eA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 250
ht-degree: 0%

---

# ホットスポットと画像マップ{#hotspots-and-image-maps}

ビューアは、AEM AssetsのDynamic Mediaでホットスポットを作成した場所に、メインビュー上にホットスポットアイコンをオンデマンドで表示します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メイン ビューア領域の&#x200B;**CSS プロパティ**

ホットスポットアイコンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7carouselviewer .s7imagemapeffect .s7icon
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>CSS スプライトを使用している場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local">個のCSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンの幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンの高さ： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 56 x 56 ピクセルのホットスポットアイコンを設定し、2つの異なるアイコンの状態ごとに異なる画像を表示します。

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

画像マップ領域の&#x200B;**CSS プロパティ**

画像マップ領域のアピアランスは、次のCSS クラスセレクターで制御されます。

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景</span> </p> </td> 
   <td colname="col2"> <p>画像マップ領域の塗りつぶしカラー。 </p> <p>この色は、<span class="codeph"> #RRGGBB </span>、<span class="codeph"> RGB（R,G,B） </span>または<span class="codeph"> RGBA （R,G,B,A） </span>形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>画像マップ領域の塗りつぶしカラー。 </p> <p>この色は、<span class="codeph"> #RRGGBB </span>、<span class="codeph"> RGB（R,G,B） </span>または<span class="codeph"> RGBA （R,G,B,A） </span>形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の境界線スタイル。 「<span class="codeph"> width </span> <span class="codeph"> solid color </span>」として指定する必要があります。ここでは、<span class="codeph"> width </span>はピクセルで表され、<span class="codeph"> color </span>は<span class="codeph"> #RRGGBB </span>、<span class="codeph"> RGB（R,G,B） </span>または<span class="codeph"> RGBA （R,G,B） </span>として指定されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 1 ピクセルの黒い境界線を持つ透明な画像マップ領域を設定します。

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

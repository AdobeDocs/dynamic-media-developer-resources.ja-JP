---
title: ホットスポットと画像マップ
description: ビューアは、ホットスポットが元々AEM Assetsの Dynamic Media でオンデマンドで作成された場所で、メインビューにホットスポットアイコンを表示します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# ホットスポットと画像マップ{#hotspots-and-image-maps}

ビューアは、ホットスポットが元々AEM Assetsの Dynamic Media でオンデマンドで作成された場所で、メインビューにホットスポットアイコンを表示します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

ホットスポットアイコンの外観は、次の CSS クラスセレクターで制御します。

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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 関する </a> を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 2 つの異なるアイコンの状態のそれぞれに異なる画像を表示する、56 x 56 ピクセルのホットスポットアイコンを設定します。

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

**画像マップ領域の CSS プロパティ**

画像マップ領域の外観は、次の CSS クラスセレクターで制御します。

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
   <td colname="col1"> <p> <span class="codeph"> background </span> </p> </td> 
   <td colname="col2"> <p>画像マップ領域の塗りつぶしの色。 </p> <p>この色 <span class="codeph">、RGB（R,G,B） </span> または <span class="codeph"> RGBA （R,G,B,A） </span> の形式 <span class="codeph">#RRGGBB </span> で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>画像マップ領域の塗りつぶしの色。 </p> <p>この色 <span class="codeph">、RGB（R,G,B） </span> または <span class="codeph"> RGBA （R,G,B,A） </span> の形式 <span class="codeph">#RRGGBB </span> で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の境界線のスタイル。 幅 <span class="codeph"></span> をピクセル単位で表す <span class="codeph"> 幅 </span> <span class="codeph"> 単色 </span>」として指定する必要があります。<span class="codeph"> 色 </span> は、<span class="codeph"> #RRGGBB </span>、<span class="codeph"> RGB（R,G,B） </span>、または <span class="codeph"> RGBA （R,G,B,A） </span> です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 1 ピクセルの黒い境界線を持つ透明画像マップ領域を設定する

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

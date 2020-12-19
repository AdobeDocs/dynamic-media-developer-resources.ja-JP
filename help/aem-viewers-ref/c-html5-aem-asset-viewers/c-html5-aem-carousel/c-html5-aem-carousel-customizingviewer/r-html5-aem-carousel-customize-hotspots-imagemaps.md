---
description: メイン表示の上に、AEM AssetsのDynamic Mediaで最初にホットスポットが作成されたオンデマンドの場所に、ホットスポットアイコンが表示されます。
seo-description: メイン表示の上に、AEM AssetsのDynamic Mediaで最初にホットスポットが作成されたオンデマンドの場所に、ホットスポットアイコンが表示されます。
seo-title: ホットスポットと画像マップ
solution: Experience Manager
title: ホットスポットと画像マップ
topic: Dynamic media
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# ホットスポットと画像マップ{#hotspots-and-image-maps}

メイン表示の上に、AEM AssetsのDynamic Mediaで最初にホットスポットが作成されたオンデマンドの場所に、ホットスポットアイコンが表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

ホットスポットアイコンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7carouselviewer .s7imagemapeffect .s7icon
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>CSSスプライトを使用している場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンの高さ </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 56 x 56ピクセルのホットスポットアイコンを設定し、アイコンの2つの状態ごとに異なる画像を表示します。

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

**画像マップ領域のCSSプロパティ**

画像マップ領域の外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>画像マップ領域の塗りのカラー </p> <p>この色は、<span class="codeph"> #RRGGBB </span>、<span class="codeph"> RGB(R,G,B) </span>または<span class="codeph"> RGBA(R,G,B,A) </span>形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>画像マップ領域の塗りのカラー </p> <p>この色は、<span class="codeph"> #RRGGBB </span>、<span class="codeph"> RGB(R,G,B) </span>または<span class="codeph"> RGBA(R,G,B,A) </span>形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の境界線のスタイル " <span class="codeph">幅</span> <span class="codeph">べた塗り色</span>"として指定します。<span class="codeph">幅</span>はピクセル単位で表し、<span class="codeph">色</span>は<span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,Gb) </span>または<span class="codeph"> RGBA(R,G,B,A) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 1ピクセルの黒い境界線の透明な画像マップ領域を設定します。

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```


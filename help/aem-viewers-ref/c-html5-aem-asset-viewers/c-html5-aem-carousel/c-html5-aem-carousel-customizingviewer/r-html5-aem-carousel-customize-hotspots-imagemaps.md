---
description: AEM Assetsのダイナミックメディアでホットスポットが最初に作成されたオンデマンドの場所に、メインビューの上にホットスポットアイコンが表示されます。
seo-description: AEM Assetsのダイナミックメディアでホットスポットが最初に作成されたオンデマンドの場所に、メインビューの上にホットスポットアイコンが表示されます。
seo-title: ホットスポットと画像マップ
solution: Experience Manager
title: ホットスポットと画像マップ
topic: Dynamic media
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# ホットスポットと画像マップ{#hotspots-and-image-maps}

AEM Assetsのダイナミックメディアでホットスポットが最初に作成されたオンデマンドの場所に、メインビューの上にホットスポットアイコンが表示されます。

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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>CSSスプライトを使用している場合、アートワークスプライト内の位置。 </p> <p>CSSスプライ <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> トを参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンの高さ </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 56 x 56ピクセルのホットスポットアイコンを設定し、2つの異なるアイコンの状態ごとに異なる画像を表示します。

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
   <td colname="col1"> <p> <span class="codeph"> 背景 </span> </p> </td> 
   <td colname="col2"> <p>画像マップ領域の塗りのカラー </p> <p>この色は、 <span class="codeph"> #RRGGBB、 </span>RGB(R,G,B)ま <span class="codeph"> たは </span>RGBA(R,G,B,A)形式で指定し <span class="codeph"></span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>画像マップ領域の塗りのカラー </p> <p>この色は、 <span class="codeph"> #RRGGBB、 </span>RGB(R,G,B)ま <span class="codeph"> たは </span>RGBA(R,G,B,A)形式で指定し <span class="codeph"></span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の境界線のスタイル " <span class="codeph"> solid color"と指定します。ここでは、ピクセル数を </span> # <span class="codeph"> width </span>、RGBを#BB <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>rgbを表します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 1ピクセルの黒い境界線を持つ透明な画像マップ領域を設定します。

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```


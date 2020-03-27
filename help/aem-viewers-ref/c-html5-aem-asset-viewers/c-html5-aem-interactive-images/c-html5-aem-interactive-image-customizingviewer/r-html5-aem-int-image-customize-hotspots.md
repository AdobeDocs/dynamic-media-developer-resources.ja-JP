---
description: AEM Assetsのダイナミックメディアでホットスポットが最初に作成されたオンデマンドの場所に、メインビューの上にホットスポットアイコンが表示されます。
seo-description: AEM Assetsのダイナミックメディアでホットスポットが最初に作成されたオンデマンドの場所に、メインビューの上にホットスポットアイコンが表示されます。
seo-title: ホットスポット
solution: Experience Manager
title: ホットスポット
topic: Dynamic media
uuid: 79c4d128-e24a-43b0-8e18-13b588eb396e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# ホットスポット{#hotspots}

AEM Assetsのダイナミックメディアでホットスポットが最初に作成されたオンデマンドの場所に、メインビューの上にホットスポットアイコンが表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

ホットスポットアイコンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactiveimage .s7imagemapeffect .s7icon
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


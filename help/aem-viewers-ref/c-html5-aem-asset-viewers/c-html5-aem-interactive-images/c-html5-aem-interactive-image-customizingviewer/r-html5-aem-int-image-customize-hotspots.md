---
description: ビューアには、AEM AssetsのDynamic Mediaでホットスポットが最初にオーサリングされたオンデマンドの場所に、メインビューの上にホットスポットアイコンが表示されます。
solution: Experience Manager
title: ホットスポット
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブ画像
role: Developer,User
exl-id: ec1d9a91-e189-470a-abe2-4f33686905e7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# ホットスポット{#hotspots}

ビューアには、AEM AssetsのDynamic Mediaでホットスポットが最初にオーサリングされたオンデマンドの場所に、メインビューの上にホットスポットアイコンが表示されます。

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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>ホットスポットアイコンのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>CSSスプライトを使用する場合は、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
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

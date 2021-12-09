---
title: お気に入りメニュー
description: コントロールバーに、お気に入りメニューのドロップダウンリストが表示されます。 このパネルは、ボタンと、ユーザーがボタンをクリックまたはタップすると展開するパネルで構成されます。 このパネルには、個々のお気に入りツールが含まれています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3c90320-b6fc-4a43-b75f-d39234b1e73c
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# お気に入りメニュー{#favorites-menu}

コントロールバーに、お気に入りメニューのドロップダウンリストが表示されます。 このパネルは、ボタンと、ユーザーがボタンをクリックまたはタップすると展開するパネルで構成されます。 このパネルには、個々のお気に入りツールが含まれています。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビューアのユーザインターフェイスにおけるお気に入りメニューの位置とサイズは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7favoritesmenu
```

**お気に入りメニューボタンの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーの上からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> 左側の次のボタンまたは行の最初のボタンの場合はコントロールバーの左側への距離。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — コントロールバーの上部から 4 ピクセル、最も近いボタンから 10 ピクセルの位置に、サイズが 28 x 28 ピクセルのお気に入りメニューを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

お気に入りメニューボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**お気に入りボタンの CSS プロパティ**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 4 つのボタンの状態ごとに異なる画像を表示するお気に入りメニューボタンを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

個々のお気に入りアイコンを含むパネルの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**お気に入りメニューパネルの CSS プロパティ**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>パネルの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 透明色を持つパネルを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

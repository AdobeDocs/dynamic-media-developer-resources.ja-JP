---
description: コントロールバーに、お気に入りメニューのドロップダウンリストが表示されます。 ボタンと、ユーザーがボタンをクリックまたはタップすると展開されるパネルで構成されます。 このパネルには、個々のお気に入りツールが含まれています。
solution: Experience Manager
title: お気に入りメニュー
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,Business Practitioner
exl-id: 129a8451-f634-44ad-adb1-f30d2621cb29
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# お気に入りメニュー{#favorites-menu}

コントロールバーに、お気に入りメニューのドロップダウンリストが表示されます。 ボタンと、ユーザーがボタンをクリックまたはタップすると展開されるパネルで構成されます。 このパネルには、個々のお気に入りツールが含まれています。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビューアユーザインターフェイス内のお気に入りメニューの位置とサイズは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7favoritesmenu
```

**お気に入りメニューボタンのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーの上からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> 左側の次のボタンまたは（このボタンが行の最初のボタンである場合は）コントロールバーの左側までの距離です。 </p> </td> 
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

例 — コントロールバーの上部から4ピクセル、最も近いボタンの左側から10ピクセルの位置に配置し、サイズが28 x 28ピクセルのお気に入りメニューを設定します。

```
.s7ecatalogsearchviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

お気に入りメニューボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton
```

**お気に入りボタンのCSSプロパティ**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、 `state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 4つのボタンの状態ごとに異なる画像を表示するお気に入りメニューボタンを設定します。

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

個々のお気に入りアイコンを含むパネルの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel
```

**お気に入りメニューパネルのCSSプロパティ**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>パネルの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 透明色を持つパネルを設定します。

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

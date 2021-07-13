---
description: 検索結果パネルは、上部の検索入力ボックスと、情報メッセージまたは検索結果が表示されるメイン領域で構成されます。
solution: Experience Manager
title: 検索結果パネル
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 1%

---

# 検索結果パネル{#search-results-panel}

検索結果パネルは、上部の検索入力ボックスと、情報メッセージまたは検索結果が表示されるメイン領域で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

パネルがアクティブな場合、ビューアのユーザインターフェイスは半透明の塗りで覆われます。 この塗りのカラーと不透明度は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>オーバーレイのカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明  </span> </p> </td> 
   <td colname="col2"> <p>カラーの不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

検索結果パネルは、使用可能なビューアの高さを常にすべて占有します。 ただし、幅を設定することはできます。 幅は、ピクセルの絶対値に設定できます。これは、中サイズと大サイズのブレークポイントのデフォルト設定です。 または、幅を100%に設定して、検索結果パネルをビューア領域全体に表示することもできます。 パネルの幅は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**検索結果スペースのCSSプロパティ**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 検索結果スペースの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 大サイズと中サイズのブレークポイントに250ピクセル幅の検索結果パネルを設定し、小サイズのブレークポイントにフルサイズのパネルを使用するには、次のように記述します。

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

検索結果パネルの上部は、検索入力ボックス専用です。 入力ボックスの側面のパディングは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**検索入力コンテナのCSSプロパティ**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> 入力ボックスの周囲のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

検索入力フィールドは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**検索入力フィールドのCSSプロパティ**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>検索入力フィールドの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left  </span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドの境界と入力テキストの間の内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>検索入力フィールドの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>検索入力フィールドの余白 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>テキストフォントのサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 高さが0ピクセル、テキストフォントが14ピクセルの検索入力フィールドを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

デフォルトでは、検索入力フィールドの左側にある検索ボタンは、以下のCSSクラスセレクターを使用して制御します。

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**検索入力ボタンのCSSプロパティ**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>「鏡のよう」アイコン画像のURL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-size  </span> </p> </td> 
   <td colname="col2"> <p>「鏡のよう」アイコンのサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンの余白。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 26 x 26ピクセルの「鏡のよう」アイコンを含む検索ボタンを設定するには、次のように記述します。サイズが30ピクセル、境界線が1ピクセルの場合：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

機能を最初に呼び出すと、検索結果パネルにテキストプロンプトが表示される場合があります。 また、検索結果が返されなかった場合にメッセージを表示します。 どの場合でも、テキストは検索結果パネルのメイン部分に表示され、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**検索情報のCSSプロパティ**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> テキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>テキストフォントの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>テキストの水平方向の整列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>フォントテキストのサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このテキストパネルでは、 `state`属性セレクターがサポートされます。このセレクターは、異なるスタイルを異なるテキストメッセージに適用するのに使用できます。 特に、 `state='prompt'`は、パネルを初めて呼び出したときに表示されるテキストプロンプトに対応します。`state='results'`は、検索ヒットに関する情報を含むテキストに対応します。と`state='no_results'`は、検索クエリが結果を返さなかった場合に表示されるテキストに対応します。

メッセージテキストはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 18ピクセルのグレーのフォントを使用するテキストパネルを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

検索結果は、検索ヒットがあるページの単一列または単一行のサムネールとしてレンダリングされます。 検索結果サムネールの間隔は、以下のCSSクラスセレクターを使用して制御します。

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**サムネールのセルのCSSプロパティ**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周囲の垂直方向のマージンのサイズ。 実際のサムネールの間隔は、 <span class="codeph"> .s7thumbcell </span>に設定された上下のマージンの合計になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 10ピクセル間隔を設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

個々のサムネールの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**サムネールのCSSプロパティ**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>サムネールの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 215 x 129ピクセルで、初期設定の境界線がライトグレー、選択された境界線がダークグレーのサムネールを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

サムネールラベルの外観は、以下のCSSクラスセレクターを使用して制御します。

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**ラベルのCSSプロパティ**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> テキストカラー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>テキストフォントの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>テキストフォントのサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 12ピクセル、グレー、Helveticaフォントを使用するラベルを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

マウス入力を使用するシステムでは、検索結果パネルの下部に2つのスクロールボタンが表示され、ユーザーが検索結果をスクロールします。 上下のスクロールボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

CSSのtop、left、bottomおよびrightプロパティを使用してスクロールボタンを配置することはできません。 代わりに、ビューアのロジックによって自動的に配置されます。

**上下スクロールボタンのCSSプロパティ**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの高さ。 </p> </td> 
  </tr> 
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
>このボタンでは、 `state`属性セレクターがサポートされます。このセレクターは、 `"up"`、 `"down"`、 `"over"`および`"disabled"`の各ボタンの状態に異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 125 x 35ピクセルで、状態ごとに異なるアートワークを持つ上スクロールボタンを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```

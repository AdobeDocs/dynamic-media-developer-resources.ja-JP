---
title: 検索結果パネル
description: 検索結果パネルは、上部の検索入力ボックスと、情報メッセージまたは検索結果が表示されるメイン領域で構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# 検索結果パネル{#search-results-panel}

検索結果パネルは、上部の検索入力ボックスと、情報メッセージまたは検索結果が表示されるメイン領域で構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

パネルがアクティブな場合、ビューアのユーザーインターフェイスは半透明の塗りつぶしで覆われます。 この塗りつぶしのカラーと不透明度は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
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
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>オーバーレイの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p>カラーの不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

検索結果パネルは、常に、使用可能なすべてのビューアの高さを占めます。 ただし、幅を設定することはできます。 幅は絶対ピクセル値に設定できます。この値は、中程度のサイズと大きいサイズのブレークポイントのデフォルト設定です。 または、幅を 100% に設定すると、検索結果パネルがビューア領域全体に表示されるようになります。 パネルの幅は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**検索結果空間の CSS プロパティ**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> 検索結果のスペースの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 幅 250 ピクセルの検索結果パネルを大および中サイズのブレークポイントに設定し、小サイズのブレークポイントでフルサイズのパネルを使用する

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

検索結果パネルの上部は、検索入力ボックス専用です。 入力ボックスの端のパディングは、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**検索入力コンテナの CSS プロパティ**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p> 入力ボックスの周囲のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

検索入力フィールドは、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**検索入力フィールドの CSS プロパティ**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>検索入力フィールドの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left </span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドの境界と入力テキストの間の内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>検索入力フィールドの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>検索入力フィールドのマージン </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>テキストフォントのサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 0 ピクセルの高さと 14 ピクセルのテキストフォントを使用して検索入力フィールドを設定するには：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

デフォルトで「looking glass」の形式の検索入力フィールドの左側にある検索ボタンは、次の CSS クラスセレクターで制御されます。

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**検索入力ボタンの CSS プロパティ**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>「鏡の中の」アイコン画像への URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-size </span> </p> </td> 
   <td colname="col2"> <p>「ルッキング グラス」アイコンのサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンのボーダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンの余白。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 26 x 26 ピクセルの「Looking Glass」アイコンと、30 ピクセルのサイズで 1 ピクセルの境界線を持つ検索ボタンを設定するには：

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

フィーチャが最初に呼び出されたときに、検索結果パネルにテキスト プロンプトが表示される場合があります。 また、ユーザーの検索が結果を返さなかった場合もメッセージが表示されます。 どの場合でも、テキストは検索結果パネルのメイン部分に表示され、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**検索情報の CSS プロパティ**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> テキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>テキストフォントの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>テキストの水平方向の配置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントテキストのサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このテキストパネルでは、`state` 属性セレクターがサポートされており、これを使用して、様々なテキストメッセージに異なるスタイルを適用できます。 特に、`state='prompt'` は、パネルが初めて呼び出されたときに表示されるテキストプロンプトに対応しています。 `state='results'` は、検索ヒット数に関する情報を含むテキストに対応します。 最後に、`state='no_results'` は、検索クエリが結果を返さなかった場合に表示されるテキストに対応します。

メッセージテキストはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 – グレーの 18 ピクセルフォントを使用するテキストパネルを設定するには：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

検索結果は、検索ヒットを含むページの 1 列または 1 行のサムネールとしてレンダリングされます。 検索結果のサムネール間の間隔は、次の CSS クラスセレクターで制御します。

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**サムネールセルの CSS プロパティ**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周囲の垂直方向の余白のサイズ。 実際のサムネールの間隔は、.s7thumbcell </span> に設定された上下の余白 <span class="codeph"> 合計と等しくなります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 10 ピクセル間隔を設定するには：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

個々のサムネールの外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**サムネールの CSS プロパティ**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>サムネールのボーダー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 215 x 129 ピクセルのサムネールで、デフォルトの境界線が薄いグレーで、選択した境界線が濃いグレーになるように設定するには：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

サムネールラベルの外観は、次の CSS クラスセレクターで制御します。

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**ラベルの CSS プロパティ**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> テキストのカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>テキストフォントの名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>テキストフォントのサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 12 ピクセル、グレー、Helvetica® フォントを使用するラベルを設定するには：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

マウス入力を使用するシステムでは、ユーザーが検索結果をスクロールすると、検索結果パネルの下部に 2 つのスクロールボタンが表示されます。 上下のスクロールボタンの外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

CSS の top、left、bottom、right プロパティを使用してスクロールボタンを配置することはできません。 代わりに、ビューアロジックによって自動的に配置されます。

**スクロールアップボタンとスクロールダウンボタンの CSS プロパティ**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>スクロール ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ール <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`"up"`、`"down"`、`"over"`、`"disabled"` のボタン状態に異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

ボタンのツールチップはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 – 125 x 35 ピクセルで、状態ごとに異なるアートワークを持つスクロールアップボタンを設定するには：

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

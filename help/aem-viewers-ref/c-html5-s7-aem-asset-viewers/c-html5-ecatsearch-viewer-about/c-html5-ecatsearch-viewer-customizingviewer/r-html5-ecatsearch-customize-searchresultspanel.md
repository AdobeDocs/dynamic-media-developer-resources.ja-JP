---
title: 検索結果パネル
description: 検索結果パネルは、上部の検索入力ボックスと、情報メッセージや検索結果が表示されるメインエリアで構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
TQID: 'https://experienceleague.adobe.com/VVRqhgxbkQOHlerVRDGNaHL-tM6elPDs-Vqotij43mg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 955
ht-degree: 0%

---

# 検索結果パネル{#search-results-panel}

検索結果パネルは、上部の検索入力ボックスと、情報メッセージや検索結果が表示されるメインエリアで構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メイン ビューア領域の&#x200B;**CSS プロパティ**

パネルがアクティブな場合、ビューアのユーザーインターフェイスは半透明の塗りで覆われています。 この塗りつぶしの色と不透明度は、次のCSS クラスセレクターで制御されます。

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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>オーバーレイの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">不透明度</span> </p> </td> 
   <td colname="col2"> <p>カラーの不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

検索結果パネルは、常に使用可能なすべてのビューアの高さを占めます。 ただし、幅は設定できます。 幅は絶対ピクセル値に設定できます。これは、中サイズおよび大サイズのブレークポイントのデフォルト設定です。 または、幅を100%に設定して、検索結果パネルをビューアエリア全体に表示することもできます。 パネルの幅は、次のCSS クラスセレクターによって制御されます。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

検索結果スペースの&#x200B;**CSS プロパティ**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> 検索結果スペースの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 大きくて中程度のサイズのブレークポイントに250 ピクセル幅の検索結果パネルを設定し、小さなサイズのブレークポイントにフルサイズのパネルを使用するには：

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

検索結果パネルの上部は、検索入力ボックス専用です。 入力ボックスの側面のパディングは、次のCSS クラスセレクターによって制御されます。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

検索入力コンテナの&#x200B;**CSS プロパティ**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> 入力ボックスの周囲をパディングします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

検索入力フィールドは、次のCSS クラスセレクターによって制御されます。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

検索入力フィールドの&#x200B;**CSS プロパティ**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>検索入力フィールドの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング左</span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドの境界と入力テキストの間の内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>検索入力フィールドの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p>検索入力フィールドのマージン </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>テキストフォントのサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 0 ピクセルの高さと14 ピクセルのテキストフォントを使用して検索入力フィールドを設定するには、次の手順を実行します。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

デフォルトで「鏡」の形で検索入力フィールドの左側にある検索ボタンは、次のCSS クラスセレクターによって制御されます。

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

検索入力ボタンの&#x200B;**CSS プロパティ**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>「鏡」アイコン画像のURL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景サイズ </span> </p> </td> 
   <td colname="col2"> <p>「鏡」アイコンのサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p>検索入力ボタンのマージン。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 26 x 26 ピクセルの「ガラスを見る」アイコンで検索ボタンを設定するには、次の手順に従います。サイズは30 ピクセルで、境界線は1 ピクセルです。

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

最初に機能が呼び出されたときに、検索結果パネルにテキストプロンプトが表示されることがあります。 また、ユーザーの検索で結果が返されなかった場合にもメッセージが表示されます。 いずれの場合も、テキストは検索結果パネルのメイン部分に表示され、次のCSS クラスセレクターによって制御されます。

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

検索情報の&#x200B;**CSS プロパティ**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p> テキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>テキストフォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>横組みテキストの整列： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントテキストのサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このテキストパネルでは、`state`属性セレクターをサポートしています。これは、異なるテキストメッセージに異なるスタイルを適用するために使用できます。 特に、`state='prompt'`は、パネルが初めて呼び出されたときに表示されるテキストプロンプトに対応しています。 `state='results'`は、検索ヒットに関する情報を含むテキストに対応します。 最後に、検索クエリが結果を返さなかった場合に表示されるテキストに`state='no_results'`が対応します。

メッセージテキストはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – グレーの18 ピクセルフォントを使用するテキストパネルを設定するには：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

検索結果は、検索ヒットを含むページの1列または1行のサムネールとしてレンダリングされます。 検索結果のサムネール間の間隔は、次のCSS クラスセレクターで制御されます。

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**サムネールセルのCSS プロパティ**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの垂直余白のサイズ。 実際のサムネールの間隔は、<span class="codeph"> .s7thumbcell </span>に設定された上余白と下余白の合計に等しくなります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 10 ピクセルの間隔を設定するには：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

個々のサムネールの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**サムネールのCSS プロパティ**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>サムネールの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 215 x 129 ピクセルのサムネールを設定するには、明るいグレーのデフォルトの境界線と濃いグレーの選択した境界線があります。

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

サムネールラベルの外観は、次のCSS クラスセレクターで制御されます。

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

ラベルの&#x200B;**CSS プロパティ**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p> テキストの色： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>テキストフォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
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

マウス入力を使用するシステムでは、検索結果パネルの下部に2つのスクロールボタンが表示され、ユーザーは検索結果をスクロールできます。 上下のスクロールボタンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

CSSの上部、左、下部、右のプロパティを使用してスクロールボタンを配置することはできません。 代わりに、ビューアリジックによって自動的に配置されます。

**スクロールアップおよびスクロールダウン ボタンのCSS プロパティ**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは`state`属性セレクターをサポートしています。このセレクターを使用すると、`"up"`、`"down"`、`"over"`、および`"disabled"`のボタン状態に異なるスキンを適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

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

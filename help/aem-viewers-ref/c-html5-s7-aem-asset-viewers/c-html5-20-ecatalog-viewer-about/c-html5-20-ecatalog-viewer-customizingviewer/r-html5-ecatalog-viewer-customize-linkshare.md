---
description: リンクツールは、ソーシャル共有パネルに追加されるボタンと、ツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
seo-description: リンクツールは、ソーシャル共有パネルに追加されるボタンと、ツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
seo-title: リンク共有
solution: Experience Manager
title: リンク共有
topic: Dynamic media
uuid: 80ecbaca-9092-40b6-bb24-4b233356de3f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 2%

---


# リンク共有{#link-share}

リンクツールは、ソーシャル共有パネルに追加されるボタンと、ツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

リンク共有ボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkshare
```

**リンク共有ツールのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> ボタンの特定の状態に対して表示する画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

CSSクラスに`display:none` CSSプロパティを設定すると、ソーシャル共有パネルからボタンを削除できます。

ボタンのツールチップをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 28 x 28ピクセルで、ボタンの4つの状態ごとに異なる画像を表示するリンク共有ボタンを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7ecatalogviewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7ecatalogviewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7ecatalogviewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

ダイアログボックスがアクティブなときのWebページをカバーする背景オーバーレイは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7backoverlay
```

**背景オーバーレイのCSSプロパティ**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity  </span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイの不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイのカラー </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 不透明度70 %のグレーの背景オーバーレイを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

デフォルトでは、モーダルなダイアログボックスがデスクトップシステムでは画面中央に表示され、タッチデバイスではWebページ領域全体に表示されます。 どのような場合でも、ダイアログボックスの位置とサイズはコンポーネントで管理されます。 ダイアログボックスは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialog
```

**ダイアログボックスのCSSプロパティ**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径（ダイアログボックスがブラウザー全体に表示されない場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>ダイアログボックスの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>ダイアログボックスがブラウザーウィンドウ全体に表示される場合は、設定しないか、100 %に設定する必要があります（タッチデバイスではこのモードを推奨）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>ダイアログボックスがブラウザーウィンドウ全体に表示される場合は、設定しないか、100 %に設定する必要があります（タッチデバイスではこのモードを推奨）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — タッチデバイスで、ブラウザーウィンドウ全体を使用し、背景色が白であるダイアログボックスを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

ダイアログボックスのヘッダーは、アイコン、タイトルテキストおよび閉じるボタンで構成されます。 ヘッダーのコンテナは、

```
.s7ecatalogviewer .s7linkdialog .s7dialogheader
```

**ダイアログボックスヘッダーのCSSプロパティ**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテンツの内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

アイコンとタイトルテキストは、追加のコンテナにまとめられます。このアイコンは、

```
.s7ecatalogviewer .s7linkdialog .s7dialogheader .s7dialogline
```

**ダイアログの線のCSSプロパティ**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーのアイコンとタイトルの内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのアイコンは、以下のCSSクラスセレクターを使用して制御します

```
.s7ecatalogviewer .s7linkdialog .s7dialogheadericon
```

**ダイアログボックスのヘッダーアイコンのCSSプロパティ**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>アイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>アイコンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>アイコン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのタイトルは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogheadertext
```

**ダイアログボックスのヘッダーテキストのCSSプロパティ**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-重み付け  </span> </p> </td> 
   <td colname="col2"> <p>フォント重み付け </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>フォントの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>テキストの内部のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

閉じるボタンは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7closebutton
```

**閉じるボタンのCSSプロパティ**

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーのコンテナを基準とした垂直方向のボタン位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーのコンテナを基準とした水平方向のボタン位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>ボタンの内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>状態ごとのボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

「閉じる」ボタンのツールチップとダイアログボックスのタイトルをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — パディング、22 x 12ピクセルのアイコン、太字の16ポイントのタイトルおよび28 x 28ピクセルの閉じるボタンを設定し、ダイアログボックスのコンテナの上から2ピクセル、右から2ピクセルの位置に配置するには、次のように記述します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogviewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogviewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogviewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogviewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

ダイアログボックスのフッターは、「キャンセル」ボタンで構成されます。 フッターのコンテナは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogfooter
```

**ダイアログボックスのフッターのCSSプロパティ**

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p> フッターとダイアログボックスのそれ以外の部分を視覚的に区切るために使用できる境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

フッターには、ボタンを保持する内側のコンテナがあります。 これは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogbuttoncontainer
```

**ダイアログボックスのボタンコンテナのCSSプロパティ**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> フッターとボタンの間の内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「すべて選択」ボタンは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogactionbutton
```

このボタンは、デスクトップシステムでのみ使用できます。

**「すべて選択」ボタンのCSSプロパティ**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 状態ごとのボタンのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 状態ごとのボタンの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>「すべて選択」ボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

「キャンセル」ボタンは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogcancelbutton
```

**ダイアログボックスの「キャンセル」ボタンのCSSプロパティ**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> 状態ごとのボタンのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 状態ごとのボタンの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

さらに、両方のボタンは同じCSSクラスを共有します。このCSSクラスには、他のダイアログボックスのボタンと同じCSS設定を含めることができます。

```
.s7ecatalogviewer .s7linkdialog .s7dialogfooter .s7button
```

**ボタンのCSSプロパティ**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-重み付け  </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォント重み付け。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントサイズ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p> ボタン内のテキストの高さ。 垂直方向揃えに影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow  </span> </p> </td> 
   <td colname="col2"> <p>ドロップシャドウ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの右マージン。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ボタンのツールヒントをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 64 x 34の「キャンセル」ボタンがあり、テキストカラーと背景色がボタンの状態ごとに異なるダイアログボックスフッターを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

ダイアログのメイン領域（ヘッダーとフッターの間）には、ダイアログのコンテンツが含まれます。 どのような場合でも、コンポーネントがこの領域の幅を管理します。CSSで設定することはできません。 ダイアログのメイン領域は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogviewarea
```

**ダイアログボックスの表示領域のCSSプロパティ**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスのメイン領域の高さ。 ダイアログボックスがデスクトップモードで動作する場合にのみ指定します。 ダイアログボックスがブラウザーウィンドウ全体を占めるようにサイズ設定される場合は適用されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>ダイアログボックスのメイン領域の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外側のマージン。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 高さが300ピクセルで、マージンが10ピクセルで、白の背景を使用するダイアログボックスのメイン領域を設定するには、次のように記述します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、コンテナ内に配置します。このコンテンツは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogbody
```

**ダイアログボックスの本体のCSSプロパティ**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 10ピクセルのパディングがあるフォームコンテンツを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスのフォーム内の静的なラベルはすべて、以下を使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialoglabel
```

このクラスは、ラベルのサイズや位置の制御には適していません。このクラスは、フォームユーザーインターフェイスの様々な場所のテキストに適用できるからです。

**ダイアログボックスのラベルのCSSプロパティ。 **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-重み付け  </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォント重み付け </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントサイズ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>ラベルのテキストカラー </p> </td> 
  </tr> 
 </tbody> 
</table>

ダイアログボックスのラベルをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — グレー、太字、9ピクセルのフォントとなるようにすべてのラベルを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

リンクの上部に表示されるテキストコピーのサイズは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialoginputwide
```

**ダイアログボックスの広い入力フィールドのCSSプロパティ**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>テキストの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が430ピクセルで、下部に10ピクセルのパディングがあるテキストコピーを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

共有リンクはコンテナでラップし、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialoginputcontainer
```

**ダイアログボックスの入力コンテナのCSSプロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>共有リンクコンテナの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 埋め込みコードテキストの周囲に9ピクセルのパディングがある1ピクセルのグレーの境界線を設定するには、次のように記述します。

```
.s7ecatalogviewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

共有リンク自体は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7linkdialog .s7dialoglink
```

**ダイアログボックス共有リンクのCSSプロパティ**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>共有リンクの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 共有リンクの幅を450ピクセルに設定するには、次のように記述します。

```
.s7ecatalogviewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```


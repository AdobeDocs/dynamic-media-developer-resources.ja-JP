---
title: 埋め込み共有
description: 埋め込み共有ツールは、ソーシャル共有パネルに追加されるボタンと、このツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、Social 共有ツールで完全に管理されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 2ed2db55-824c-40b6-8747-6b9b8792f5db
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '2606'
ht-degree: 2%

---

# 埋め込み共有{#embed-share}

埋め込み共有ツールは、ソーシャル共有パネルに追加されるボタンと、このツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、Social 共有ツールで完全に管理されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

埋め込み共有ボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embedshare
```

**埋め込み共有ツールの CSS プロパティ**

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

このボタンを Social 共有パネルから削除するには、 `display:none` CSS プロパティを CSS クラスに設定する。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 28 x 28 ピクセルで、4 つのボタンの状態ごとに異なる画像を表示する埋め込み共有ボタンを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7ecatalogviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7ecatalogviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7ecatalogviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

ダイアログボックスがアクティブなときに Web ページを覆う背景オーバーレイは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7backoverlay
```

**背景オーバーレイの CSS プロパティ**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイの不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 不透明度 70%を持つグレーの背景オーバーレイを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

デフォルトでは、モーダルダイアログボックスはデスクトップシステムの画面の中央に表示され、タッチデバイスの Web ページ領域全体に表示されます。 どの場合でも、ダイアログボックスの位置とサイズはコンポーネントによって管理されます。 このダイアログボックスは、以下の CSS クラスセレクターを使用して制御します。

```
.s7embeddialog .s7dialog
```

**ダイアログボックスの CSS プロパティ**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径（ダイアログボックスがブラウザ全体に表示されない場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>ダイアログボックスの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ダイアログボックスがブラウザーウィンドウ全体に表示される場合は、未設定にするか、100%に設定する必要があります（このモードはタッチデバイスで推奨されます）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ダイアログボックスがブラウザーウィンドウ全体に表示される場合は、未設定にするか、100%に設定する必要があります（このモードはタッチデバイスで推奨されます）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — タッチデバイスでブラウザーウィンドウ全体を使用し、背景が白いダイアログボックスを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

ダイアログボックスのヘッダーは、アイコン、タイトルテキストおよび閉じるボタンで構成されます。 ヘッダーコンテナは、を使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader
```

**ダイアログボックスヘッダーの CSS プロパティ**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテンツの内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

アイコンとタイトルテキストは、

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**ダイアログの行の CSS プロパティ**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーアイコンとタイトルの内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのアイコンは、以下の CSS クラスセレクターを使用して制御します

```
.s7ecatalogviewer .s7embeddialog .s7dialogheadericon
```

**ダイアログボックスヘッダーのアイコンの CSS プロパティ**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>アイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>アイコンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>アイコン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのタイトルは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogheadertext
```

**ダイアログボックスのヘッダーテキストの CSS プロパティ**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内部テキストパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

閉じるボタンは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7closebutton
```

**閉じるボタンの CSS プロパティ**

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテナを基準とした垂直方向のボタン位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテナを基準とした水平方向のボタン位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>ボタンの内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
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

例 — パディング、24 x 14 ピクセルのアイコン、太字の 16 ポイントのタイトルを含むダイアログボックスヘッダーを設定するには、次のように記述します。 また、28 x 28 ピクセルの閉じるボタンで、ダイアログコンテナの上から 2 ピクセル、右から 2 ピクセルの位置に配置されます。

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

ダイアログフッターは、「キャンセル」ボタンで構成されます。 フッターコンテナは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter
```

**ダイアログボックスフッターの CSS プロパティ**

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p> フッターとダイアログボックスの残りの部分を視覚的に区切るために使用できる境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

フッターには、ボタンを保持する内部コンテナがあります。 これは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogbuttoncontainer
```

**ダイアログボックスのボタンコンテナの CSS プロパティ**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> フッターとボタンの間の内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「すべて選択」ボタンは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton
```

このボタンは、デスクトップシステムでのみ使用できます。

**「すべて選択」ボタンの CSS プロパティ**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>「すべて選択」ボタンでは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

「キャンセル」ボタンは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton
```

**ダイアログボックスの「キャンセル」ボタンの CSS プロパティ**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

また、両方のボタンは、他のダイアログボックスのボタンと同じ CSS 設定を含むことができる、共通の CSS クラスを共有します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter .s7button
```

**ボタンの CSS プロパティ**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行の高さ </span> </p> </td> 
   <td colname="col2"> <p> ボタン内のテキストの高さ。 垂直方向の位置揃えに影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>ドロップシャドウ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>ボタンの右余白。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 64 x 34 の「キャンセル」ボタン、82 x 34 の「すべて選択」ボタンを含み、ボタンの状態ごとに異なるテキスト色と背景色を持つダイアログボックスフッターを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

メインダイアログ領域（ヘッダーとフッターの間）には、スクロール可能なダイアログコンテンツと、右側のスクロールパネルが含まれています。 どのような場合でも、コンポーネントがこの領域の幅を管理するので、CSS で設定することはできません。 ダイアログのメイン領域は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogviewarea
```

**ダイアログボックス表示領域の CSS プロパティ**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスのメイン領域の高さです。 この値は、ダイアログボックスがデスクトップモードで動作する場合にのみ指定する必要があります。 ダイアログボックスのサイズがブラウザーウィンドウ全体を占めるように設定されている場合は、この機能は適用されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>ダイアログボックスのメイン領域の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外側の余白。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 高さが 300 ピクセルで、マージンが 10 ピクセルで、白の背景を使用するダイアログボックスのメイン領域を設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、コンテナ内に配置され、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogbody
```

このコンテナの高さがメインのダイアログボックス領域より大きい場合は、コンポーネントによって垂直スクロールが自動的に有効になります。

**ダイアログボックスの本文の CSS プロパティ**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 10 ピクセルのパディングを持つフォームコンテンツを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスフォーム内のすべての静的ラベルは、を使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialoglabel
```

このクラスは、フォームユーザーインターフェイスの様々な場所のテキストに適用できるので、ラベルのサイズや位置の制御には適していません。

**ダイアログボックスのラベルの CSS プロパティ。 **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー </span> </p> </td> 
   <td colname="col2"> <p>ラベルのテキストの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ダイアログボックスのラベルはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — グレー、太字、9 ピクセルのフォントにすべてのラベルを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

埋め込みコードの上部に表示されるテキストコピーのサイズは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputwide
```

**ダイアログボックスの入力全体のフィールドの CSS プロパティ**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 430 ピクセルで、下部に 10 ピクセルのパディングがあるテキストコピーを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

埋め込みコードはコンテナにまとめられ、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer
```

**ダイアログボックスの入力コンテナの CSS プロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードコンテナの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードコンテナの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 埋め込みコードテキストの周囲に 1 ピクセルのグレーの境界線を設定するには、埋め込みコードテキストの幅を 430 ピクセルにし、10 ピクセルのパディングを持つようにします。

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

実際の埋め込みコードテキストは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer
```

**ダイアログボックスの入力コンテナの CSS プロパティ**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap </span> </p> </td> 
   <td colname="col2"> <p>ワードラッピングのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 使用する埋め込みコードを設定するには `break-word` ワードラッピング：

```
.s7ecatalogviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

埋め込みサイズのラベルとドロップダウンは、ダイアログボックスの下部に配置され、コンテナに配置されます。このコンテナは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel
```

**ダイアログボックス埋め込みサイズパネルの CSS プロパティ**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 10 ピクセルのパディングを持つ埋め込みサイズパネルを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

埋め込みサイズラベルのサイズと整列は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel
```

**ダイアログボックス埋め込みサイズパネルの CSS プロパティ**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>垂直方向のラベルの整列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ラベルの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 上揃えで幅が 80 ピクセルの埋め込みサイズラベルを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

埋め込みサイズコンボボックスの幅は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7combobox
```

**コンボボックスの CSS プロパティ**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>コンボボックスの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>コンボボックスは、 `expanded` 可能な値を持つ属性セレクター `true` および `false`. この `true` 値は、コンボボックスに事前に定義された埋め込みサイズの 1 つが表示される場合に使用されます。そのため、使用可能なすべての幅を取る必要があります。 この `false` 値は、コンボボックスでカスタムサイズオプションが選択されている場合に使用されます。そのため、カスタムの幅と高さの入力フィールド用のスペースができるように縮小する必要があります。

例 — 定義済みのアイテムを表示する場合は幅が 300 ピクセル、カスタムサイズを表示する場合は幅が 110 ピクセルの埋め込みサイズコンボボックスを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

コンボボックスのテキストの高さは、特別な内部要素で定義し、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**コンボボックステキストの CSS プロパティ**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>コンボボックスのテキストの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 埋め込みサイズコンボボックスのテキストの高さを 40 ピクセルに設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

コンボボックスの右側に「ドロップダウン」ボタンがあり、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**コンボボックスボタンの CSS プロパティ**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>コンボボックス内の垂直方向のボタン位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>コンボボックス内の水平方向のボタン位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
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

例 — 28 x 28 ピクセルで、状態ごとに別々の画像を持つドロップダウンボタンを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

コンボボックスを開いたときに表示される埋め込みサイズのリストを含むパネルは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7comboboxdropdown
```

パネルのサイズと位置は、コンポーネントによって制御されます。 CSS を使用して変更することはできません。

**コンボボックスドロップダウンの CSS プロパティ**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>パネルの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 1 ピクセルのグレーの境界線を持つコンボボックスパネルを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

以下の CSS クラスセレクターを使用して制御される、ドロップダウンパネル内の単一の項目です。

```
.s7ecatalogviewer .s7embeddialog .s7dropdownitemanchor
```

**ドロップダウン項目アンカーの CSS プロパティ**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>項目の背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — コンボボックスパネル項目の背景が白になるように設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

コンボボックスパネル内の選択項目の左側に表示されるチェックマークは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7checkmark
```

**チェックマークボックスの CSS プロパティ**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>アイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>アイコンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>項目の画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — チェックマークアイコンを 25 x 25 ピクセルに設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

埋め込みサイズコンボボックスで「カスタムサイズ」オプションが選択されている場合、ダイアログボックスの右側に 2 つの追加の入力フィールドが表示され、ユーザーがカスタム埋め込みサイズを入力できます。 これらのフィールドは、以下の CSS クラスセレクターを使用して制御するコンテナにまとめられます。

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsizepanel
```

**ダイアログボックスのカスタムサイズパネルの CSS プロパティ**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p> 埋め込みサイズコンボボックスからの距離。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — コンボボックスの右側に 20 ピクセルのカスタムサイズ入力フィールドパネルを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

各カスタムサイズ入力フィールドは、境界線をレンダリングし、フィールド間の余白を設定するコンテナにまとめられます。 これは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsize
```

**ダイアログボックスのカスタムサイズの CSS プロパティ**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 余白 </span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドの余白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドのパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 1 ピクセルのグレーの境界線、マージン、パディングを持ち、幅が 70 ピクセルのカスタムサイズ入力フィールドを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

垂直方向のスクロールが必要な場合は、ダイアログボックスの右端近くのパネル内にスクロールバーがレンダリングされます。このスクロールバーは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogscrollpanel
```

**ダイアログボックスのスクロールパネルの CSS プロパティ**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>スクロールパネルの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 44 ピクセルのスクロールパネルを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

スクロールバー領域の外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar
```

**スクロールバーの CSS プロパティ**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>スクロールバーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p> スクロールパネルの上部からの垂直方向のスクロールバーのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p> スクロールパネルの下端からの垂直方向のスクロールバーのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> スクロールパネルの右端からの水平方向のスクロールバーのオフセット。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 28 ピクセルで、スクロールパネルの上、右、下から 8 ピクセルのマージンがあるスクロールバーを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

スクロールバートラックは、上下のスクロールボタンの間の領域です。 このコンポーネントは、トラックの位置と高さを自動的に設定します。 トラックは、以下の CSS クラスセレクターを使用して制御します

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**スクロールバートラックの CSS プロパティ**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>トラッキングの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 背景色を追跡します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 28 ピクセルで、背景がグレーのスクロールバートラックを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

スクロールバーサムは、スクロールトラック領域内で垂直方向に移動します。 垂直位置は、コンポーネントロジックによって完全に制御されます。 ただし、サムの高さは、コンテンツの量に応じて動的に変化するわけではありません。 サムの高さやその他の要素は、以下の CSS クラスセレクターを使用して設定できます。

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**スクロールバーサムの CSS プロパティ**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>サムの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>サムの高さ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>トラックの上部との間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> トラックの下端との間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 指定されたサムの状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムは `state` 属性セレクター。サムの状態ごとに異なるスキンを適用するのに使用できます。 `up`, `down`, `over`、および `disabled`.

例 — 28 x 45 ピクセルで、上下に 10 ピクセルのマージンがあり、状態ごとに異なるアートワークを持つスクロールバーサムを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

上下のスクロールボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

CSS を使用してスクロールボタンを配置することはできません `top`, `left`, `bottom`、および `right` プロパティ。 代わりに、ビューアのロジックによって自動的に配置が決まります。

**上下のスクロールボタンの CSS プロパティ**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>これらのボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。 `up`, `down`, `over`、および `disabled`.

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 28 x 32 ピクセルで、状態ごとに異なるアートワークを持つスクロールボタンを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

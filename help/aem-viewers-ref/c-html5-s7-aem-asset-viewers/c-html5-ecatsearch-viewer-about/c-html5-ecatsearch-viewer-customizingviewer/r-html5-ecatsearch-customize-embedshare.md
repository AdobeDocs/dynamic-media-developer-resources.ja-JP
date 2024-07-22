---
title: 共有を埋め込む
description: 埋め込み共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティベートされたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 82117b6e-c0be-4538-90ab-8def7521b49c
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '2640'
ht-degree: 0%

---

# 共有を埋め込む{#embed-share}

埋め込み共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティベートされたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

埋め込み共有ボタンの外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embedshare
```

**埋め込み共有ツールの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅 </p> </td> 
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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ール <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

CSS クラスに CSS プロパティを設定することで、ソーシャル共有パネルからボタン `display:none` 削除することができます。

ボタンのツールチップはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 – 28 x 28 ピクセルで、4 つの異なるボタン状態ごとに異なる画像を表示する埋め込み共有ボタンを設定するには：

```
.s7ecatalogsearchviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

ダイアログボックスがアクティブな場合に web ページを覆う背景のオーバーレイは、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7backoverlay
```

**背景オーバーレイの CSS プロパティ**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイの不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>背景のオーバーレイカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 背景オーバーレイを 70% の不透明度でグレーに設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

デフォルトでは、モーダルダイアログボックスはデスクトップシステムでは画面の中央に表示され、タッチデバイスでは web ページ領域全体を取ります。 どの場合でも、ダイアログボックスの位置とサイズはコンポーネントで管理されます。 このダイアログボックスは、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialog
```

**ダイアログボックスの CSS プロパティ**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径（ダイアログボックスがブラウザー全体を取らない場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>ダイアログボックスの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>未設定または 100% に設定する必要があります。この場合、ダイアログボックスはブラウザーウィンドウ全体を取り込みます（タッチデバイスでは、このモードをお勧めします）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>未設定または 100% に設定する必要があります。この場合、ダイアログボックスはブラウザーウィンドウ全体を取り込みます（タッチデバイスでは、このモードをお勧めします）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ブラウザーウィンドウ全体を使用し、タッチデバイスの背景が白くなるようにダイアログボックスを設定するには：

```
.s7ecatalogsearchviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

ダイアログボックスヘッダーは、アイコン、タイトルテキスト、閉じるボタンから構成されます。 ヘッダーコンテナは、

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader
```

**ダイアログボックスヘッダーの CSS プロパティ**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテンツの内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

アイコンとタイトルテキストは、で制御される追加のコンテナにラップされます

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**ダイアログラインの CSS プロパティ**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーアイコンとタイトルの内部パディング </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーアイコンは、次の CSS クラスセレクターで制御します

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadericon
```

**ダイアログボックスのヘッダーアイコンの CSS プロパティ**

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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ール <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのタイトルは、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadertext
```

**ダイアログボックスのヘッダーテキストの CSS プロパティ**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>フォントの線幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内部テキストのパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「閉じる」ボタンは、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton
```

**閉じるボタンの**の CSS プロパティ

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテナに対する垂直方向のボタンの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテナに対する水平方向のボタンの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>ボタンの内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ール <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

ボタンのツールチップはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 – パディング、24 x 14 ピクセルのアイコン、太字の 16 ポイントのタイトルを含むダイアログヘッダーを設定する 最後に、28 x 28 ピクセルの「閉じる」ボタンが、上から 2 ピクセル、ダイアログコンテナの右から 2 ピクセルの位置に表示されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

ダイアログフッターは、「キャンセル」ボタンで構成されています。 フッターコンテナは、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter
```

**ダイアログボックスのフッター**の CSS プロパティ

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p> フッターをダイアログボックスの他の部分と視覚的に区別する際に使用する境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

フッターには、ボタンを保持する内部コンテナがあります。 次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbuttoncontainer
```

**ダイアログボックスのボタンコンテナの CSS プロパティ**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p> フッターとボタンの間の内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「すべてを選択」ボタンは、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton
```

ボタンは、デスクトップシステムでのみ使用できます。

**「すべてを選択」ボタンの CSS プロパティ**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンのテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンの背景色 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>「すべてを選択」ボタンでは、`state` 属性セレクターがサポートされており、異なるボタン状態に異なるスキンを適用するために使用できます。

「キャンセル」ボタンは、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton
```

**ダイアログボックスのキャンセルボタンの CSS プロパティ**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンのテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンの背景色 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

さらに、両方のボタンは共通の CSS クラスを共有します。このクラスには、他のダイアログボックスのボタンと同じ CSS 設定を含めることができます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter .s7button
```

**ボタンの CSS プロパティ**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントの線幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> ボタン内のテキストの高さ。 垂直方向の位置揃えに影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ボックスの影の </span> </p> </td> 
   <td colname="col2"> <p>ドロップシャドウ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>ボタンの右の余白。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ボタンのツールチップはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 – 64 x 34 の「キャンセル」ボタン、82 x 34 の「すべてを選択」ボタンを使用し、テキストカラーと背景色がボタンの状態ごとに異なるダイアログボックスのフッターを設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

メインダイアログ領域は、ヘッダーとフッターの間に、スクロール可能なダイアログコンテンツと、右側のスクロールパネルを含んでいます。 いずれの場合も、コンポーネントはこの領域の幅を管理し、CSS で設定することはできません。 メインダイアログ領域は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogviewarea
```

**ダイアログボックスの表示エリアの CSS プロパティ **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p> メイン ダイアログ ボックス領域の高さです。 このオプションは、ダイアログボックスがデスクトップモードで動作する場合にのみ指定してください。 ダイアログ ボックスのサイズがブラウザ ウィンドウ全体に表示される場合は、この設定は適用されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>メインのダイアログボックス領域の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外側余白。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – メインダイアログボックス領域の高さを 300 ピクセルに設定し、余白を 10 ピクセルにして背景を白くするには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、次の CSS クラスセレクターで制御されるコンテナ内に存在します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbody
```

このコンテナの高さがメインダイアログボックスの領域よりも大きく表示される場合、コンポーネントによって垂直スクロールが自動的に有効になります。

**ダイアログボックスの本文の CSS プロパティ**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – フォームコンテンツの 10 ピクセルのパディングを設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスのフォームのすべての静的ラベルは、次のコントロールで制御されます

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoglabel
```

このクラスは、フォームユーザーインターフェイスの様々な場所でテキストに適用できるので、ラベルのサイズや位置の制御には適していません。

**ダイアログボックスのラベルの CSS プロパティ。 **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントの線幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>ラベルのテキストの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ダイアログ ボックスのラベルはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 – すべてのラベルを 9 ピクセルのフォントを使用してグレー、太字に設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

埋め込みコードの上に表示されるテキストコピーのサイズは、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputwide
```

**ダイアログボックス入力全体フィールドの CSS プロパティ**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – テキストコピーの幅を 430 ピクセルに設定し、下部に 10 ピクセルのパディングを含める場合：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

埋め込みコードはコンテナにラップされ、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer
```

**ダイアログボックス入力コンテナの CSS プロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードコンテナの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードコンテナを囲むボーダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 埋め込みコードテキストの周囲に 1 ピクセルグレーの境界線を設定する場合は、幅を 430 ピクセルにし、10 ピクセルのパディングにします。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

実際の埋め込みコードテキストは、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer
```

**ダイアログボックス入力コンテナの CSS プロパティ**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ワードラップ </span> </p> </td> 
   <td colname="col2"> <p>ワードラップのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ワードラッピングを使用するように埋め込みコードを設定する `break-word` は：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

埋め込みサイズのラベルとドロップダウンはダイアログボックスの下部にあり、次の CSS クラスセレクターで制御されるコンテナに配置します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel
```

**ダイアログボックス埋め込みサイズパネルの CSS プロパティ**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 10 ピクセルのパディングを持つ埋め込みサイズパネルを設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

埋め込みサイズラベルのサイズと配置は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel
```

**ダイアログボックス埋め込みサイズパネルの CSS プロパティ**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 垂直方向の位置揃え </span> </p> </td> 
   <td colname="col2"> <p>垂直方向のラベルの配置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ラベルの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 埋め込みサイズ ラベルを上揃えおよび幅 80 ピクセルに設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

埋め込みサイズ コンボボックスの幅は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox
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
>コンボボックスでは、`true` および `false` の可能な値を持つ `expanded` 属性セレクターがサポートされています。 値 `true` は、コンボボックスに事前定義済みの埋め込みサイズのいずれかが表示されるときに使用されるので、使用可能なすべての幅をとる必要があります。 この値 `false`、コンボ ボックスで [ サイズの設定 ] オプションが選択されている場合に使用されます。この値は、幅と高さのカスタム入力フィールドのスペースを確保するために小さくする必要があります。

例 – 事前定義済みの項目を表示する場合に埋め込みサイズ コンボボックスの幅を 300 ピクセルに、カスタムサイズを表示する場合に幅 110 ピクセルに設定する：

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

コンボボックステキストの高さは、特別な内部要素によって定義され、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxtext
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

例 – 埋め込みサイズ コンボボックスのテキストの高さを 40 ピクセルに設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

コンボボックスの右側には「ドロップダウン」ボタンがあり、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**コンボボックスボタンの CSS プロパティ**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>コンボボックス内の垂直方向のボタンの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>コンボボックス内の水平ボタンの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅 </p> </td> 
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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ール <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

例 – ドロップダウンボタンを 28 x 28 ピクセルに設定し、状態ごとに個別の画像を用意するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

コンボボックスを開くと表示される埋め込みサイズのリストを含むパネルは、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7comboboxdropdown
```

パネルのサイズと位置は、コンポーネントによって制御されます。 CSS を使用して変更することはできません。

**コンボボックスドロップダウンの CSS プロパティ**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>パネルの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンボボックスパネルの境界線を 1 ピクセルのグレーに設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

ドロップダウンパネル内の 1 つの項目。次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dropdownitemanchor
```

**ドロップダウンアイテムアンカーの CSS プロパティ**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>項目の背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンボボックスのパネル項目の背景を白に設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

コンボボックスパネル内で選択された項目の左側に表示されるチェックマーク。以下の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7checkmark
```

**チェックボックスの CSS プロパティ**

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
   <td colname="col2"> <p>項目画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ール <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – チェックマークアイコンを 25 x 25 ピクセルに設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

埋め込みサイズ コンボボックスで「カスタムサイズ」オプションを選択すると、ダイアログボックスの右側に 2 つの追加入力フィールドが表示され、ユーザーがカスタム埋め込みサイズを入力できます。 これらのフィールドは、次の CSS クラスセレクターで制御されるコンテナにラップされます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsizepanel
```

**ダイアログボックスのカスタムサイズパネルの CSS プロパティ**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> 「埋め込みサイズ」コンボボックスからの距離。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – カスタムサイズの入力フィールドパネルをコンボボックスの右側の 20 ピクセルに設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

各カスタムサイズ入力フィールドは、境界線をレンダリングし、フィールド間の余白を設定するコンテナにラップされます。 次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsize
```

**ダイアログボックスのカスタムサイズの CSS プロパティ**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> フィールドの余白を入力します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドのパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – カスタムサイズの入力フィールドに 1 ピクセルのグレーの境界線、余白、パディングを設定し、幅を 70 ピクセルにするには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

垂直方向のスクロールが必要な場合、スクロールバーはダイアログボックスの右端の近くのパネルにレンダリングされます。このパネルは、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogscrollpanel
```

**ダイアログボックスのスクロールパネルの CSS プロパティ**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>パネル幅をスクロールします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – スクロールパネルの幅を 44 ピクセルに設定する

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

スクロールバー領域の外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar
```

**スクロールバーの CSS プロパティ**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>スクロール バーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p> スクロールパネルの上部からオフセットされた垂直スクロールバー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p> スクロールパネルの下部からオフセットされた垂直スクロールバー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> 水平スクロールバーをスクロールパネルの右端からオフセットします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 幅 28 ピクセルで、スクロールパネルの上、右および下から 8 ピクセルのマージンを持つスクロールバーを設定するには、次のようにします。

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

スクロールバートラックは、上部と下部のスクロールボタンの間の領域です。 トラックの位置と高さが自動的に設定されます。 トラックは、次の CSS クラスセレクターで制御します

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**スクロールバートラックの CSS プロパティ**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>トラックの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> 背景色を追跡する。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 幅 28 ピクセルで背景がグレーのスクロールバーのトラックを設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

スクロールバーの親指は、スクロールトラック領域内で垂直に移動します。 垂直方向の位置は、コンポーネントのロジックによって完全に制御されます。 ただし、コンテンツの量に応じて親指の高さが動的に変化することはありません。 親指の高さやその他の側面は、次の CSS クラスセレクターで設定できます。

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**スクロールバーのサムネールの CSS プロパティ**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>親指の幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>親指の高さ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>トラックの上部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> トラックの下部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 特定のサムネール状態で表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ール <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb は、`up`、`down`、`over`、`disabled` などの異なるサムステートに異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

例 – 28 x 45 ピクセルのスクロールバーの親指を設定し、上下に 10 ピクセルのマージンがあり、状態ごとに異なるアートワークを持つ場合：

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

上部と下部のスクロールボタンの外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

CSS `top`、`left`、`bottom` および `right` プロパティを使用してスクロールボタンを配置することはできません。 代わりに、ビューアロジックによって自動的に配置されます。

**上下のスクロールボタンの CSS プロパティ**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅 </p> </td> 
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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト </a> ール <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>これらのボタンは、`state` 属性セレクターをサポートしています。このセレクターを使用して、ボタンの状態（`up`、`down`、`over`、`disabled`）に応じて異なるスキンを適用できます。

ボタンのツールチップはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 – 28 x 32 ピクセルで、状態ごとに異なるアートワークを持つスクロールボタンを設定するには：

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

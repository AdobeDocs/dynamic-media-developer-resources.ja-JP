---
title: リンク共有
description: リンク共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティベートされたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 9eb2ef38-9b86-4c60-90a2-6609cb3fcc39
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# リンク共有{#link-share}

リンク共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティベートされたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

リンク共有ボタンの外観は、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkshare
```

**リンク共有ツールの CSS プロパティ**

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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>参照： <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。異なるボタンの状態に異なるスキンを適用するために使用できます。

を設定することで、ボタンをソーシャル共有パネルから削除することができます `display:none` CSS クラスの CSS プロパティ。

ボタンのツールチップはローカライズできます。 参照： [ユーザーインターフェイス要素のローカリゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

例 – 28 x 28 ピクセルのリンク共有ボタンを設定し、4 つの異なるボタン状態のそれぞれに異なる画像を表示するには、次のようにします。

```
.s7video360viewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7video360viewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7video360viewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7video360viewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

ダイアログボックスがアクティブな場合に web ページを覆う背景のオーバーレイは、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkdialog .s7backoverlay
```

**背景オーバーレイの CSS プロパティ**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の不透明度 </span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイの不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>背景のオーバーレイカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  – 背景オーバーレイを 70% の不透明度でグレーに設定するには：

```
.s7video360viewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

デフォルトでは、モーダルダイアログボックスはデスクトップシステムでは画面の中央に表示され、タッチデバイスでは web ページ領域全体を取ります。 どの場合でも、ダイアログボックスの位置とサイズはコンポーネントで管理されます。 このダイアログボックスは、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkdialog .s7dialog
```

**ダイアログボックスの CSS プロパティ**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径（ダイアログボックスがブラウザー全体を取らない場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
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

**例** - ブラウザーウィンドウ全体を使用し、タッチデバイスの背景が白くなるようにダイアログボックスを設定するには：

```
.s7video360viewer.s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

ダイアログボックスヘッダーは、アイコン、タイトルテキスト、閉じるボタンで構成されます。 ヘッダーコンテナは、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkdialog .s7dialogheader
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

アイコンとタイトルテキストは、次の CSS クラスセレクターで制御される追加のコンテナにラップされます。

```
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline
```

**ダイアログラインの CSS プロパティ**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーアイコンとタイトルの内部パディング </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーアイコンは、次の CSS クラスセレクターで制御します

```
.s7video360viewer .s7linkdialog .s7dialogheadericon
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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>参照： <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのタイトルは、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkdialog .s7dialogheadertext
```

**ダイアログボックスのヘッダーテキストの CSS プロパティ**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>フォントの線幅。 </p> </td> 
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
   <td colname="col2"> <p>内部テキストのパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「閉じる」ボタンは、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkdialog .s7closebutton
```

**閉じるボタンの**の CSS プロパティ

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上位 </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテナに対する垂直方向のボタンの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>ボタンの内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>参照： <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。異なるボタンの状態に異なるスキンを適用するために使用できます。

閉じるボタンのツールヒントとダイアログボックスのタイトルは、ローカライズできます。 参照： [ユーザーインターフェイス要素のローカリゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**例** - パディング、22 x 12 ピクセルのアイコン、および太字の 16 ポイントのタイトルを含むダイアログボックスヘッダーを設定します。 最後に、ダイアログボックスのコンテナの上から 2 ピクセル、右から 2 ピクセルの位置にある 28 x 28 ピクセルの「閉じる」ボタンを選択します。

```
.s7video360viewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

ダイアログボックスのフッターは、「キャンセル」ボタンで構成されます。 フッターコンテナは、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkdialog .s7dialogfooter
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
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer
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

「すべてを選択」ボタンは、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkdialog .s7dialogactionbutton
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
   <td colname="col1"> <p> <span class="codeph"> 色 </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンのテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンの背景色 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>「すべてを選択」ボタンは、 `state` 属性セレクター。異なるボタンの状態に異なるスキンを適用するために使用できます。

「キャンセル」ボタンは、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkdialog .s7dialogcancelbutton
```

**ダイアログボックスの CSS プロパティ キャンセルボタン**

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
   <td colname="col1"> <p> <span class="codeph"> 色 </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンのテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンの背景色 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。異なるボタンの状態に異なるスキンを適用するために使用できます。

さらに、両方のボタンは共通の CSS クラスを共有します。このクラスには、他のダイアログボックスのボタンと同じ CSS 設定を含めることができます。

```
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button
```

**ボタンの CSS プロパティ**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントの線幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> ボタン内のテキストの高さ。 垂直方向の位置揃えに影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ボックス影 </span> </p> </td> 
   <td colname="col2"> <p>ドロップシャドウ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン （右） </span> </p> </td> 
   <td colname="col2"> <p>ボタンの右の余白。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ボタンのツールチップはローカライズできます。 参照： [ユーザーインターフェイス要素のローカリゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**例** - 64 x 34 の「キャンセル」ボタンを持つダイアログボックスのフッターを設定する場合。各ボタンの状態によって異なるテキストの色と背景の色を使用します。

```
.s7video360viewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

メインダイアログ領域には、ヘッダーとフッターの間にダイアログコンテンツが含まれています。 いずれの場合も、コンポーネントによってこの領域の幅が管理されます。CSS で設定することはできません。 メインダイアログ領域は、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkdialog .s7dialogviewarea
```

**ダイアログボックスの表示エリアの CSS プロパティ **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p> メイン ダイアログ ボックス領域の高さです。 このオプションは、ダイアログボックスがデスクトップモードで動作する場合にのみ指定してください。 ダイアログ ボックスのサイズがブラウザ ウィンドウ全体に表示される場合は、この設定は適用されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p>メインのダイアログボックス領域の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 余白 </span> </p> </td> 
   <td colname="col2"> <p>外側余白。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - メインダイアログボックス領域の高さを 300 ピクセル、マージンを 10 ピクセルに設定し、背景を白くするには：

```
.s7video360viewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

ラベルや入力フィールドなどのすべてのフォームコンテンツは、次の CSS クラスセレクターで制御されるコンテナ内に存在します。

```
.s7video360viewer .s7linkdialog .s7dialogbody
```

**ダイアログボックスの本文の CSS プロパティ**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - フォームコンテンツの 10 ピクセルのパディングを設定するには：

```
.s7interactivevideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスのフォームのすべての静的ラベルは、次のコントロールで制御されます

```
.s7video360viewer .s7linkdialog .s7dialoglabel
```

このクラスは、フォームユーザーインターフェイスの様々な場所でテキストに適用できるので、ラベルのサイズや位置の制御には適していません。

**ダイアログボックスのラベルの CSS プロパティ。 **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントの線幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 色 </span> </p> </td> 
   <td colname="col2"> <p>ラベルのテキストの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ダイアログ ボックスのラベルはローカライズできます。 参照： [ユーザーインターフェイス要素のローカリゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**例**  – すべてのラベルを 9 ピクセルのフォントを使用してグレー、太字に設定するには：

```
.s7video360viewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

リンクの上に表示されるテキストコピーのサイズは、次の CSS クラスセレクターで制御されます。

```
.s7video360viewer .s7linkdialog .s7dialoginputwide
```

**ダイアログボックスの入力全体フィールドの CSS プロパティ**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>テキストの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - テキストコピーの幅を 430 ピクセルに設定し、下部に 10 ピクセルのパディングを含めるには：

```
.s7video360viewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

共有リンクはコンテナにラップされ、次の CSS クラスセレクターで制御されます。

```
.s7video360viewer .s7linkdialog .s7dialoginputcontainer
```

**ダイアログボックスの入力コンテナの CSS プロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>リンクを共有コンテナを囲むボーダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  – 埋め込みコードテキストの周囲に 1 ピクセルのグレーの境界線を設定し、9 ピクセルのパディングを持つ：

```
.s7video360viewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

共有リンク自体は、次の CSS クラスセレクターで制御します。

```
.s7video360viewer .s7linkdialog .s7dialoglink
```

**ダイアログボックスの CSS プロパティ共有リンク**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>リンクの幅を共有します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  – 共有リンクの幅を 450 ピクセルに設定するには：

```
.s7video360viewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```

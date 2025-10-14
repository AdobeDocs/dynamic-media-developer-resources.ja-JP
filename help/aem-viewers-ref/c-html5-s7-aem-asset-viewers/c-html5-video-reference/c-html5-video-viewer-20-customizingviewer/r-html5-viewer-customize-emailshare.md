---
title: メール共有
description: メール共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティベートされたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1788e069-68dd-4960-bc49-34ffdf29991a
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '3023'
ht-degree: 0%

---

# メール共有{#email-share}

メール共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティベートされたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メール共有ボタンの外観は、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emailshare
```

**メール共有ツールの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

CSS クラスに CSS プロパティを設定することで、ソーシャル共有パネルからボタン `display:none` 削除することができます。

ボタンのツールチップはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 – 28 x 28 ピクセルのメール共有ボタンを設定します。このボタンは、4 つの異なるボタン状態ごとに異なる画像を表示します。

```
.s7videoviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7videoviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7videoviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7videoviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

ダイアログがアクティブな場合に web ページに適用される背景のオーバーレイは、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7backoverlay
```

**バックオーバーレイの CSS プロパティ**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity </span> </p> </td> 
   <td colname="col2"> <p> 背景オーバーレイの不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>背景のオーバーレイカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 背景オーバーレイを 70% の不透明度でグレーに設定するには：

```
.s7videoviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

デフォルトでは、モーダルダイアログはデスクトップシステムでは画面の中央に表示され、タッチデバイスでは web ページ領域全体を占めます。 どの場合でも、ダイアログボックスの位置とサイズはコンポーネントで管理されます。 ダイアログは、次の CSS クラスセレクターで制御されます。

```
.s7videoviewer .s7emaildialog .s7dialog
```

**ダイアログボックスの CSS プロパティ**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径（ダイアログボックスがブラウザーウィンドウ全体を取らない場合） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの背景色 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> 未設定または 100% に設定する必要があります。この場合、ダイアログはブラウザーウィンドウ全体を取り込みます（このモードはタッチデバイスで推奨されます）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p> 未設定または 100% に設定する必要があります。この場合、ダイアログはブラウザーウィンドウ全体を取り込みます（このモードはタッチデバイスで推奨されます）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ブラウザーウィンドウ全体を使用し、タッチデバイスの背景が白くなるようにダイアログを設定するには：

```
.s7videoviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

ダイアログボックスヘッダーは、アイコン、タイトルテキスト、閉じるボタンで構成されます。 ヘッダーコンテナは、次の CSS クラスセレクターで制御します

```
.s7videoviewer .s7emaildialog .s7dialogheader
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
.s7videoviewer .s7emaildialog .s7dialogheader .s7dialogline
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
.s7videoviewer .s7emaildialog .s7dialogheadericon
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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのタイトルは、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogheadertext
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
.s7videoviewer .s7emaildialog .s7closebutton
```

**閉じるボタンの**&#x200B;の CSS プロパティ

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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

閉じるボタンのツールヒントとダイアログボックスのタイトルは、ローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 – パディング、24 x 17 ピクセルのアイコン、太字の 16 ポイントのタイトル、28 x 28 ピクセルの「閉じる」ボタンを使用してダイアログヘッダーを設定する。 最後に、ダイアログコンテナの上から 2 ピクセル、右から 2 ピクセルの位置を指定します。

```
.s7videoviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7videoviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

ダイアログフッターは、「キャンセル」と「メールを送信」のボタンで構成されています。 フッターコンテナは、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogfooter
```

**ダイアログボックスのフッター**&#x200B;の CSS プロパティ

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p> フッターをダイアログボックスの他の部分と視覚的に区別する際に使用する境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

フッターには、両方のボタンを保持する内部コンテナがあります。 次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogbuttoncontainer
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

「キャンセル」ボタンは、次の CSS クラスセレクターで制御されます。

```
.s7videoviewer .s7emaildialog .s7dialogcancelbutton
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

「メールを送信」ボタンは、次の CSS クラスセレクターで制御されます。

```
.s7videoviewer .s7emaildialog .s7dialogactionbutton
```

**ダイアログボックスのアクションボタンの CSS プロパティ**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
.s7videoviewer .s7emaildialog .s7dialogfooter .s7button
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

ボタンのツールチップはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 – 64 x 34 キャンセルボタンと 82 x 34 の「メールを送信」ボタンを使用し、テキストカラーと背景色がボタンの状態ごとに異なるダイアログボックスフッターを設定するには：

```
.s7videoviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

メインダイアログ領域は、ヘッダーとフッターの間に、スクロール可能なダイアログコンテンツと、右側のスクロールパネルを含んでいます。 いずれの場合も、コンポーネントはこの領域の幅を管理し、CSS で設定することはできません。 メインダイアログ領域は、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogviewarea
```

**ダイアログボックスの表示エリアの CSS プロパティ &#x200B;**

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

>[!NOTE]
>
>メインダイアログボックス領域では、オプションの `state` 属性セレクターをサポートしています。 メールフォームが送信され、ダイアログボックスに確認メッセージが表示されると、`sendsuccess` に設定されます。 確認メッセージが小さい場合は、この属性セレクターを使用して、確認メッセージが表示されるときにダイアログボックスの高さを低くすることができます。

例 – 最初にメインダイアログボックス領域の高さを 300 ピクセル、確認メッセージが表示されたときに高さを 100 ピクセルに設定し、余白が 10 ピクセルにして背景が白くするには：

```
.s7videoviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7videoviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、で制御されるコンテナに格納されます

```
.s7videoviewer .s7emaildialog .s7dialogbody
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
.s7videoviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスのフォームは、1 行ごとに入力されます。各行には、フォームコンテンツの一部（ラベルやテキスト入力フィールドなど）が含まれます。 単一のフォーム行は、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**ダイアログボックスのラインの CSS プロパティ**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内側の行のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ダイアログボックスフォームの各行に 10 ピクセルのパディングを設定するには、次のようにします。

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

ダイアログボックスのフォームのすべての静的ラベルは、次のコントロールで制御されます

```
.s7videoviewer .s7emaildialog .s7dialoglabel
```

このクラスは、フォームユーザーインターフェイスの様々な場所でテキストに適用できるので、ラベルのサイズや位置の制御には適していません。

**ダイアログボックスのラベルの CSS プロパティ。 &#x200B;**

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

ダイアログ ボックスのラベルはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 – すべてのラベルを 9 ピクセルのフォントを使用してグレー、太字に設定するには：

```
.s7videoviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

フォーム入力フィールドの左側に表示されるすべての静的ラベルは、次のように制御されます。

```
.s7videoviewer .s7emaildialog .s7dialoginputlabel
```

**ダイアログボックスの入力ラベルの CSS プロパティ**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>静的ラベルの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>テキストの水平方向の配置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>ラベルの静的な余白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>ラベルの静的パディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 入力フィールドラベルの幅を 50 ピクセル、右揃え、10 ピクセルのパディングを持ち、右側に 10 ピクセルの余白を持つように設定するには：

```
.s7videoviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

各フォーム入力フィールドは、入力フィールドの周囲にカスタムの境界線を適用できるコンテナにラップされます。 次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialoginputcontainer
```

**ダイアログボックス入力コンテナの CSS プロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>入力フィールドコンテナの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>入力フィールドコンテナは、オプションの `state` 属性セレクターをサポートしています。 ユーザーが入力データ形式を誤り、インライン検証に失敗した場合、`verifyerror` に設定されます。 この属性セレクターを使用すると、フォーム内の誤ったユーザー入力をハイライト表示できます。

ダイアログボックスの本文の左側のラベルから右端に広がるほとんどの入力フィールド（「from」フィールドと「message」フィールドを含む）は、次のように制御されます。

```
.s7videoviewer .s7emaildialog .s7dialoginputwide
```

**ダイアログボックス入力全体フィールドの CSS プロパティ**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「宛先」入力フィールドは、右側の「メールを削除」ボタン用のスペースを割り当てるので、より狭くなります。 次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialoginputshort
```

**ダイアログボックス入力の短いフィールドの CSS プロパティ**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – すべての入力フィールドの周囲に 9 ピクセルのパディングを行う 1 ピクセルグレーの境界線を持つフォームを設定する 検証に失敗したフィールドに同じボーダーを赤で表示するには、幅が 250 ピクセルの「To」入力フィールドを使用し、残りの入力フィールドに幅が 300 ピクセルの場合：

```
.s7videoviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7videoviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

メールメッセージの入力フィールドも、次のように制御されます。

```
.s7videoviewer .s7emaildialog .s7dialogmessage
```

このクラスを使用すると、基になる `TEXTAREA` 要素に特定のプロパティを設定できます。

**ダイアログボックスメッセージの CSS プロパティ**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>メッセージの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ワードラップ </span> </p> </td> 
   <td colname="col2"> <p>ワードラップのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – メールメッセージの高さを 50 ピクセルに設定し、ワードラッピング `break-word` 使用するには：

```
.s7videoviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

「別のメールアドレスを追加」ボタンを使用すると、ユーザーがメールフォームに複数のアドレスを追加できます。 次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton
```

**ダイアログボックスの「メールアドレスを追加」ボタンの CSS プロパティ**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>各状態のボタンのテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>ボタン領域内でのボタンの画像位置。 </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>ボタン内のテキストの高さ。 垂直方向の整列に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>テキストの水平方向の配置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

ボタンのツールチップはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 – 「別のメールアドレスを追加」ボタンの高さを 25 ピクセルに設定するには、右揃えの 12 ポイントの太字フォントを使用し、状態ごとに異なるテキストカラーと画像を使用します。

```
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

「削除」ボタンを使用すると、ユーザーがメールフォームから追加のアドレスを削除できます。 次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton
```

**ダイアログボックスの削除メールボタンの CSS プロパティ**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
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
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

ボタンのツールチップはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 – 「削除」ボタンを 25 x 25 ピクセルに設定し、状態ごとに異なる画像を使用するには：

```
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7videoviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

共有されるコンテンツは、ダイアログボックスの本文の下部に表示され、サムネール、タイトル、接触チャネル URL、説明が含まれます。 次で制御されるコンテナにラップされます。

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**ダイアログボックスのコンテンツ &#x200B;** の CSS プロパティ

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>コンテナの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 下のコンテナを 1 ピクセルの点線の境界線を持ち、パディングを含まないように設定するには：

```
.s7videoviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

サムネール画像は、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogthumbnail
```

`background-image` プロパティは、コンポーネントロジックによって設定されます。

**ダイアログボックスのサムネール画像の CSS プロパティ**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>サムネイルの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>サムネイルの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 垂直方向の位置揃え </span> </p> </td> 
   <td colname="col2"> <p>垂直方向揃えサムネール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – サムネールを 90 x 60 ピクセルに設定し、10 ピクセルのパディングで上揃えにする

```
.s7videoviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

コンテンツのタイトル、接触チャネル、説明は、さらにコンテンツサムネールの右側のパネルにグループ化されます。 次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialoginfopanel
```

**ダイアログボックス情報パネルの CSS プロパティ**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>パネル幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンテンツ情報パネルの幅を 300 ピクセルに設定するには：

```
.s7videoviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

コンテンツのタイトルは、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogtitle
```

**ダイアログボックスのタイトルの CSS プロパティ**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外側余白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>フォントの線幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンテンツタイトルで太字フォントを使用し、10 ピクセルの余白を設定するには：

```
.s7videoviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

コンテンツの接触チャネルは、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogorigin
```

**ダイアログボックスのコンテンツの接触チャネル**&#x200B;の CSS プロパティ

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外側余白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>フォントの線幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンテンツオリジンに 10 ピクセルの余白を設定するには：

```
.s7videoviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

コンテンツの説明は、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogdescription
```

**ダイアログボックスのコンテンツの説明の CSS プロパティ**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外側余白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>フォントの線幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 10 ピクセルの余白を持ち、9 ポイントのフォントを使用するコンテンツの説明を設定するには：

```
.s7videoviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

ユーザーが誤った入力データを入力してインライン検証が失敗した場合、またはフォームが送信されたときにダイアログボックスがエラーまたは確認メッセージをレンダリングする必要がある場合、ダイアログボックスの本文の上部にメッセージが表示されます。 次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7dialogerrormessage
```

**ダイアログボックスのエラーメッセージの CSS プロパティ**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> エラーアイコン。 デフォルトは感嘆符です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> メッセージ領域内のエラーアイコンの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>メッセージのテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>フォントの線幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> メッセージ内のテキストの高さ。 垂直方向の位置揃えに影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このメッセージでは、`state`、`verifyerror`、`senderror` の値を持つ `sendsuccess` 属性セレクターがサポートされています。 属性セレクター `verifyerror` は、インライン入力検証エラーによってメッセージが表示されたときに設定されます。`senderror` は、バックエンドのメールサービスがエラーを報告したときに設定されます。`sendsuccess` は、メールが正常に送信されたときに設定されます。 これにより、ダイアログボックスの状態に応じて異なるスタイルをメッセージに設定できます。

エラーメッセージはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 – 10 ポイントの太字フォントを使用するメッセージを設定します。 また、行の高さが 25 ピクセル、左側にパディングが 20 ピクセルである必要があります。感嘆符アイコン、エラーがある場合は赤のテキスト、成功がある場合はアイコンと緑のテキストを使用します。

```
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7videoviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

垂直方向のスクロールが必要な場合、スクロールバーはダイアログの右端近くのパネルでレンダリングされます。このパネルは、次の CSS クラスセレクターで制御されます。

```
.s7videoviewer .s7emaildialog .s7dialogscrollpanel
```

**ダイアログボックスのスクロールパネルの CSS プロパティ**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>パネル幅をスクロールします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – スクロールパネルの幅を 44 ピクセルに設定するには：

```
.s7videoviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

スクロールバー領域の外観は、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7scrollbar
```

**スクロールバーの CSS プロパティ**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> スクロールバーの幅。 </p> </td> 
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

例 – 幅 28 ピクセル、スクロールパネルの上部、右側、下部から 8 ピクセルの余白にあるスクロールバーを設定するには、次のようにします。

```
.s7videoviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

スクロールバートラックは、上部と下部のスクロールボタンの間の領域です。 トラックの位置と高さが自動的に設定されます。 トラックは、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**スクロールトラックの CSS プロパティ**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>トラックの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>トラックの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 幅 28 ピクセルで背景がグレーのスクロールバーのトラックを設定するには：

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

スクロール バーの親指は、スクロール トラック領域内で縦方向に移動します。 垂直方向の位置はコンポーネントロジックによって完全に制御されますが、コンテンツの量に応じて親指の高さが動的に変化することはありません。 次の CSS クラスセレクターを使用して、親指の高さやその他の側面を設定できます。

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**スクロールバーのサムネールの CSS プロパティ**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>親指の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>親指の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p> トラックの上部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> トラックの下部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>特定のサムネール状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb は、`state`、`up`、`down`、`over` などの異なるサムステートに異なるスキンを適用するために使用できる `disabled` 属性セレクターをサポートしています。

ボタンのツールチップはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 – 28 x 45 ピクセルのスクロールバーの親指を設定し、上部と下部に 10 ピクセルのマージンがあり、状態ごとに異なるアートワークを持つ場合：

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

上部と下部のスクロールボタンの外観は、次の CSS クラスセレクターで制御します。

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton  
  
```

**上下のスクロールボタンの CSS プロパティ**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
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
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>これらのボタンは、`state` 属性セレクターをサポートしています。このセレクターを使用して、ボタンの状態（`up`、`down`、`over`、`disabled`）に応じて異なるスキンを適用できます。

例 – 28 x 32 ピクセルで、状態ごとに異なるアートワークを持つスクロールボタンを設定するには：

```
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7videoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

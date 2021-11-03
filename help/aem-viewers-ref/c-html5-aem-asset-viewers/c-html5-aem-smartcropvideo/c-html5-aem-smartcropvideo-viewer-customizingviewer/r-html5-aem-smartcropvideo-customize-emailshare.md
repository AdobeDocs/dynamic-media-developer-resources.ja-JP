---
title: メール共有
description: 電子メール共有ツールは、ソーシャル共有パネルに追加されるボタンと、ツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、Social 共有ツールで完全に管理されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 1788e069-68dd-4960-bc49-34ffdf29991a
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '2994'
ht-degree: 2%

---

# メール共有{#email-share}

電子メール共有ツールは、ソーシャル共有パネルに追加されるボタンと、ツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、Social 共有ツールで完全に管理されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

電子メール共有ボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emailshare
```

**電子メール共有ツールの CSS プロパティ**

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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

このボタンを Social 共有パネルから削除するには、 `display:none` CSS プロパティを CSS クラスに設定する。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — 28 x 28 ピクセルで、ボタンの 4 つの状態ごとに異なる画像を表示する電子メール共有ボタンを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

ダイアログボックスがアクティブなときに Web ページを覆う背景オーバーレイは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7backoverlay
```

**背面オーバーレイの CSS プロパティ**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p> 背景オーバーレイの不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 不透明度 70%を持つグレーの背景オーバーレイを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

デフォルトでは、モーダルダイアログはデスクトップシステムの画面の中央に表示され、タッチデバイスの Web ページ領域全体に表示されます。 どの場合でも、ダイアログボックスの位置とサイズはコンポーネントによって管理されます。 ダイアログは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialog
```

**ダイアログボックスの CSS プロパティ**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径（ダイアログボックスがブラウザーウィンドウ全体に表示されない場合） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの背景色 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> ダイアログがブラウザーウィンドウ全体に表示される場合は、設定解除するか、100%に設定する必要があります（タッチデバイスではこのモードをお勧めします）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p> ダイアログがブラウザーウィンドウ全体に表示される場合は、設定を解除するか、100%に設定する必要があります（タッチデバイスではこのモードをお勧めします）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — タッチデバイスでブラウザーウィンドウ全体を使用し、背景が白であるダイアログを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

ダイアログボックスのヘッダーは、アイコン、タイトルテキストおよび「閉じる」ボタンで構成されます。 ヘッダーコンテナは、以下の CSS クラスセレクターを使用して制御します

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader
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
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader .s7dialogline
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
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadericon
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのタイトルは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadertext
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
.s7smartcropvideoviewer .s7emaildialog .s7closebutton
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

「閉じる」ボタンのツールチップとダイアログボックスのタイトルは、ローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — パディング、24 x 17 ピクセルのアイコン、太字の 16 pt タイトルを含むダイアログヘッダーを設定するには、次のように記述します。 最後に、28 x 28 ピクセルの「閉じる」ボタンを使用して、ダイアログコンテナの上から 2 ピクセル、右から 2 ピクセルの位置に配置します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

ダイアログフッターは、「キャンセル」ボタンと「電子メールを送信」ボタンで構成されます。 フッターコンテナは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter
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

フッターには、両方のボタンを保持する内部コンテナがあります。 これは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbuttoncontainer
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

「キャンセル」ボタンは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton
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
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

電子メールを送信ボタンは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton
```

**ダイアログボックスのアクションボタンの CSS プロパティ**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter .s7button
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

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — 64 x 34 の「キャンセル」ボタンと 82 x 34 の「電子メールを送信」ボタンを含むダイアログボックスフッターを設定するには、次のように記述します。 最後に、ボタンの状態ごとにテキストの色と背景色が異なります。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

メインダイアログ領域（ヘッダーとフッターの間）には、スクロール可能なダイアログコンテンツと、右側のスクロールパネルが含まれています。 どのような場合でも、コンポーネントがこの領域の幅を管理するので、CSS で設定することはできません。 ダイアログのメイン領域は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea
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

>[!NOTE]
>
>ダイアログボックスのメイン領域では、オプションの `state` 属性セレクターを使用します。 これはに設定されています。 `sendsuccess` 電子メールフォームが送信され、ダイアログボックスに確認メッセージが表示されます。 確認メッセージが小さい限り、この属性セレクターを使用して、確認メッセージが表示される際のダイアログボックスの高さを小さくすることができます。

例 — 最初は高さが 300 ピクセル、確認メッセージが表示されたときは高さが 100 ピクセルで、マージンが 10 ピクセルで、白の背景を使用するメインダイアログボックス領域を設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、を使用して制御されるコンテナ内に配置されます。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody
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
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスのフォームは 1 行ごとに入力され、各行はフォームコンテンツの一部（ラベルやテキスト入力フィールドなど）を保持します。 単一のフォーム行は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**ダイアログボックスの行の CSS プロパティ**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側の行のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 各行に 10 ピクセルのパディングを持つダイアログボックスフォームを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

ダイアログボックスフォーム内のすべての静的ラベルは、を使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoglabel
```

このクラスは、ラベルのサイズや位置の制御には適していません。このクラスは、フォームのユーザーインターフェイスの様々な場所のテキストに適用できます。

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

ダイアログボックスのラベルはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — グレー、太字、9 ピクセルのフォントにすべてのラベルを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

フォーム入力フィールドの左側に表示されるすべての静的ラベルは、以下を使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputlabel
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
   <td colname="col2"> <p>テキストの水平方向揃え。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 余白 </span> </p> </td> 
   <td colname="col2"> <p>静的ラベルの余白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>静的ラベルのパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 50 ピクセル、右揃え、パディングが 10 ピクセル、右側に 10 ピクセルのマージンがある入力フィールドラベルを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

各フォーム入力フィールドは、コンテナにまとめられます。このコンテナを使用して、入力フィールドの周囲にカスタムの境界線を設定できます。 これは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer
```

**ダイアログボックスの入力コンテナの CSS プロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>入力フィールドコンテナの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>入力フィールドコンテナではオプションがサポートされます `state` 属性セレクターを使用します。 これはに設定されています。 `verifyerror` ユーザーが入力データ形式に誤りがあり、インライン検証が失敗した場合。 この属性セレクターを使用すると、フォーム内の誤ったユーザー入力をハイライト表示できます。

左側のラベルからダイアログボックスの本文の右端まで拡大する入力フィールド（「from」フィールドと「message」フィールドを含む）のほとんどは、次を使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputwide
```

**ダイアログボックスの入力全体のフィールドの CSS プロパティ**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「宛先」入力フィールドは、右側に「電子メールを削除」ボタン用の領域が割り当てられるので、狭くなります。 これは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputshort
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

例 — 1 ピクセルのグレーの境界線を持つフォームを設定し、すべての入力フィールドの周囲に 9 ピクセルのパディングを含めるには、次のように記述します。 検証に失敗したフィールドに対して同じ境界線を赤で表示するには、幅が 250 ピクセルの「宛先」入力フィールドを使用し、残りの入力フィールドの幅を 300 ピクセルにします。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

E メールメッセージの入力フィールドは、次のアイテムも使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogmessage
```

このクラスを使用すると、基になる `TEXTAREA` 要素。

**ダイアログボックスメッセージの CSS プロパティ**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>メッセージの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap </span> </p> </td> 
   <td colname="col2"> <p>ワードラッピングのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 高さが 50 ピクセルの電子メールメッセージを設定し、 `break-word` ワードラッピング：

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

「別の電子メールアドレスを追加」ボタンを使用すると、ユーザーは電子メールフォームに複数のアドレスを追加できます。 これは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton
```

**ダイアログボックスの「電子メールアドレスを追加」ボタンの CSS プロパティ**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー </span> </p> </td> 
   <td colname="col2"> <p>各状態のボタンのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>ボタン領域内のボタン画像の位置。 </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>ボタン内のテキストの高さ。 垂直方向の位置揃えに影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>水平方向のテキスト揃え。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — 高さが 25 ピクセルの「別の電子メールアドレスを追加」ボタンを設定するには、12 ポイントの太字フォントを右揃えで使用し、状態ごとに異なるテキスト色と画像を使用します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

「削除」ボタンを使用すると、ユーザーはメールフォームから余分なアドレスを削除できます。 これは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton
```

**ダイアログボックスの「電子メールを削除」ボタンの CSS プロパティ**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
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
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — 25 x 25 ピクセルで、状態ごとに異なる画像を使用する「削除」ボタンを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

共有されるコンテンツは、ダイアログボックスの本文の下部に表示され、サムネール、タイトル、接触チャネル URL および説明が含まれます。 これは、次を使用して制御するコンテナにまとめられます。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**ダイアログボックスのコンテンツの CSS プロパティ**

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>コンテナの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 境界線が 1 ピクセル、パディングがない下部コンテナを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

サムネール画像は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogthumbnail
```

この `background-image` プロパティはコンポーネントロジックによって設定されます。

**ダイアログボックスのサムネール画像の CSS プロパティ**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>垂直方向揃えのサムネール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 90 x 60 ピクセルで、上揃えで 10 ピクセルのパディングを使用するサムネールを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

コンテンツのタイトル、起源および説明は、コンテンツのサムネールの右側のパネルにさらにグループ化されます。 これは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginfopanel
```

**ダイアログボックスの情報パネルの CSS プロパティ**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>パネルの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 300 ピクセルのコンテンツ情報パネルを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

コンテンツのタイトルは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogtitle
```

**ダイアログボックスのタイトルの CSS プロパティ**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 余白 </span> </p> </td> 
   <td colname="col2"> <p>外側の余白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 太字フォントを使用し、10 ピクセルのマージンを持つコンテンツタイトルを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

コンテンツの起源は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogorigin
```

**ダイアログボックスのコンテンツの接触チャネルの CSS プロパティ**

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 余白 </span> </p> </td> 
   <td colname="col2"> <p>外側の余白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 10 ピクセルのマージンを持つコンテンツのオリジンを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

コンテンツの説明は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogdescription
```

**ダイアログボックスのコンテンツの説明の CSS プロパティ**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 余白 </span> </p> </td> 
   <td colname="col2"> <p>外側の余白。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 10 ピクセルのマージンがあり、9 ポイントのフォントを使用するコンテンツの説明を設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

ユーザーが誤った入力データを入力し、インライン検証に失敗した場合、またはフォームの送信時にダイアログボックスでエラーまたは確認メッセージをレンダリングする必要がある場合は、ダイアログボックスの本文の上部にメッセージが表示されます。 これは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage
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
   <td colname="col1"> <p> <span class="codeph"> カラー </span> </p> </td> 
   <td colname="col2"> <p>メッセージのテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行の高さ </span> </p> </td> 
   <td colname="col2"> <p> メッセージ内のテキストの高さ。 垂直方向の位置揃えに影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このメッセージでは、 `state` 次の値を持つ属性セレクター： `verifyerror`, `senderror`、および `sendsuccess`. 値 `verifyerror` は、インライン入力検証エラーが原因でメッセージが表示される場合に設定されます。 値 `senderror` は、バックエンドの電子メールサービスがエラーを報告する際に設定されます。 この `sendsuccess` の値は、電子メールが正常に送信されたときに設定されます。 これにより、ダイアログボックスの状態に応じて異なるスタイルでメッセージをスタイル設定できます。

エラーメッセージはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — 10 ポイントの太字フォントを使用し、行の高さが 25 ピクセル、左に 20 ピクセルのパディングを使用するメッセージを設定するには、次のように記述します。 また、感嘆符アイコンを使用し、エラーが発生した場合は赤いテキストを使用し、成功した場合はアイコンと緑のテキストを使用しません。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

垂直方向のスクロールが必要な場合、スクロールバーがダイアログの右端近くのパネル内にレンダリングされます。このパネルは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogscrollpanel
```

**ダイアログボックスのスクロールパネルの CSS プロパティ**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>スクロールパネルの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 44 ピクセルのスクロールパネルを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

スクロールバー領域の外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar
```

**スクロールバーの CSS プロパティ**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> スクロールバーの幅。 </p> </td> 
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
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

スクロールバートラックは、上下のスクロールボタンの間の領域です。 このコンポーネントは、トラックの位置と高さを自動的に設定します。 トラックは、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**スクロールトラックの CSS プロパティ**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>トラックの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>トラックの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 28 ピクセルで、背景がグレーのスクロールバートラックを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

スクロールバーサムは、スクロールトラック領域内で垂直に移動します。 サムネールの垂直方向の位置は、コンポーネントのロジックによって完全に制御されますが、サムの高さはコンテンツの量に応じて動的に変化するわけではありません。 サムの高さやその他の要素は、以下の CSS クラスセレクターを使用して設定できます。

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**スクロールバーサムの CSS プロパティ**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>サムの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>サムの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p> トラックの上部との間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> トラックの下端との間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>サムの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムは `state` 属性セレクター。サムの状態ごとに異なるスキンを適用するのに使用できます。 `up`, `down`, `over`、および `disabled`.

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — 28 x 45 ピクセルで、上と下に 10 ピクセルのマージンがあり、状態ごとに異なるアートワークを持つスクロールバーサムを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

上下のスクロールボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton  
  
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
   <td colname="col2"> <p>ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>これらのボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。 `up`, `down`, `over`、および `disabled`.

例 — 28 x 32 ピクセルで、状態ごとに異なるアートワークを持つスクロールボタンを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

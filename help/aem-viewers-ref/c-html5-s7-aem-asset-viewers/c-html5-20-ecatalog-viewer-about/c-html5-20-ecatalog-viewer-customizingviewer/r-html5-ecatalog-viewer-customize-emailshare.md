---
title: メール共有
description: メール共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティブ化されたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 4c72500b-9750-4fae-9447-96cf600b31c7
TQID: 'https://experienceleague.adobe.com/ugdlpm7g0gS0bKTyktuOlhq8cOgOGvIDr8Bh-t6XGjE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 3144
ht-degree: 0%

---

# メール共有{#email-share}

メール共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティブ化されたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メール共有ボタンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emailshare
```

メール共有ツールの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

ソーシャル共有パネルからボタンを削除するには、CSS クラスに`display:none` CSS プロパティを設定します。

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 28 x 28 ピクセルのメール共有ボタンを設定し、4つの異なるボタンの状態ごとに異なる画像を表示する。

```
.s7ecatalogviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7ecatalogviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7ecatalogviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7ecatalogviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

ダイアログボックスがアクティブな場合にweb ページをカバーする背景オーバーレイは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7backoverlay
```

バックオーバーレイの&#x200B;**CSS プロパティ**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">不透明度</span> </p> </td> 
   <td colname="col2"> <p> 背景オーバーレイの不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイの色： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 背景オーバーレイを70%の不透明度でグレーに設定するには：

```
.s7ecatalogviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

デフォルトでは、モーダルダイアログはデスクトップシステムの画面の中央に表示され、タッチデバイスのweb ページ全体を表示します。 いずれの場合も、ダイアログボックスの位置とサイズはコンポーネントによって管理されます。 ダイアログは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialog
```

ダイアログボックスの&#x200B;**CSS プロパティ**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径（ダイアログボックスがブラウザーウィンドウ全体を取り込まない場合） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの背景色 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> 設定を解除するか、100%に設定する必要があります。この場合、ダイアログはブラウザーウィンドウ全体を使用します（このモードはタッチデバイスで優先されます）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p> 設定を解除するか、100%に設定する必要があります。この場合、ダイアログはブラウザーウィンドウ全体を使用します（このモードはタッチデバイスで推奨されます）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ブラウザーウィンドウ全体を使用し、タッチデバイスで白い背景を持つようにダイアログを設定するには：

```
.s7ecatalogviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

ダイアログボックスヘッダーは、アイコン、タイトルテキスト、閉じるボタンで構成されます。 ヘッダーコンテナは、次のCSS クラスセレクターで制御されます

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader
```

ダイアログボックスヘッダーの&#x200B;**CSS プロパティ**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテンツの内部パディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

アイコンとタイトルテキストは、で制御される追加のコンテナにラップされます

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader .s7dialogline
```

ダイアログ行の&#x200B;**CSS プロパティ**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーアイコンとタイトルのインナーパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーアイコンは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogheadericon
```

ダイアログボックスヘッダーアイコン **の** CSS プロパティ

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>アイコンの幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>アイコンの高さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>アイコン画像： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダータイトルは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogheadertext
```

ダイアログボックスのヘッダーテキストの&#x200B;**CSS プロパティ**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントの高さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内部テキストパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

「閉じる」ボタンは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7closebutton
```

**&#x200B; 閉じるボタン**&#x200B;のCSS プロパティ

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテナに対する垂直ボタンの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p> ヘッダーコンテナに対する水平ボタンの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>ボタンの内側パディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

閉じるボタンのツールヒントとダイアログボックスのタイトルはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – パディング、24 x 17 ピクセルのアイコン、太字の16 ポイントタイトルを含むダイアログボックスヘッダーを設定する。 最後に、28 x 28 ピクセルの「閉じる」ボタンを使用します。このボタンは、ダイアログボックスコンテナの上部から2 ピクセル、右側から2 ピクセルに配置されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

ダイアログフッターは、「キャンセル」ボタンと「メールを送信」ボタンで構成されます。 フッターコンテナは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter
```

**&#x200B; ダイアログボックスのフッター**&#x200B;のCSS プロパティ

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p> フッターをダイアログボックスの他の部分から視覚的に分離するために使用できる境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

フッターには、両方のボタンを保持するインナーコンテナがあります。 これは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogbuttoncontainer
```

ダイアログボックスボタンコンテナの&#x200B;**CSS プロパティ**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> フッターとボタン間の内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

キャンセル ボタンは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton
```

ダイアログボックスの&#x200B;**CSS プロパティのキャンセル ボタン**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

メールを送信ボタンは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton
```

ダイアログボックスアクションボタンの&#x200B;**CSS プロパティ**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 各状態のボタンの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

さらに、両方のボタンは共通のCSS クラスを共有します。このクラスには、他のダイアログボックスボタンと同じCSS設定を含めることができます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter .s7button
```

ボタンの&#x200B;**CSS プロパティ**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントの太さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>ボタンフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行の高さ</span> </p> </td> 
   <td colname="col2"> <p> ボタン内のテキスト高さ。 垂直方向の整列に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ボックス シャドウ </span> </p> </td> 
   <td colname="col2"> <p>ドロップシャドウ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右余白</span> </p> </td> 
   <td colname="col2"> <p>右ボタンのマージン。 </p> </td> 
  </tr> 
 </tbody> 
</table>

このボタンのツールヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 64 x 34 キャンセル ボタンと82 x 34 メール送信ボタンを含むダイアログボックスフッターを設定する。 テキストの色と背景色は、ボタンの状態ごとに異なります。

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

ヘッダーとフッターの間にあるメインダイアログエリアには、右側のスクロール可能なダイアログコンテンツとスクロールパネルが含まれています。 いずれの場合も、コンポーネントはこの領域の幅を管理しますが、CSSで設定することはできません。 メインダイアログ領域は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea
```

**&#x200B; ダイアログボックスの表示領域のCSS プロパティ &#x200B;**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p> メインダイアログボックス領域の高さ。 ダイアログボックスがデスクトップモードで動作する場合にのみ指定する必要があります。 ダイアログボックスのサイズがブラウザーウィンドウ全体を占める場合は適用されません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>メインダイアログボックス領域の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p>外側のマージン： </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>メインダイアログボックス領域は、オプションの`state`属性セレクターをサポートしています。 電子メールフォームが送信され、ダイアログボックスに確認メッセージが表示されたときに`sendsuccess`に設定されます。 確認メッセージが小さい限り、この属性セレクターを使用して、確認メッセージが表示されるときにダイアログボックスの高さを下げることができます。

例 – メインダイアログボックスの領域を最初に300 ピクセルの高さに、確認メッセージが表示されるときに100 ピクセルの高さに設定するには、10 ピクセルの余白を設定し、白い背景を使用します。

```
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、次のCSS クラスセレクターで制御されるコンテナ内にあります。

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody
```

このコンテナの高さがメインダイアログボックス領域よりも高いと思われる場合は、コンポーネントによって垂直スクロールが自動的に有効になります。

**&#x200B; ダイアログボックスの本文**&#x200B;のCSS プロパティ

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – フォームコンテンツを10 ピクセルパディングに設定するには：

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスフォームは行ごとに入力されます。各行には、フォームコンテンツの一部（ラベルやテキスト入力フィールドなど）が含まれます。 単一のフォーム行は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogline
```

ダイアログボックス行の&#x200B;**CSS プロパティ**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>行の内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ダイアログボックスフォームを設定して、各行に10個のピクセルパディングを設定するには、次の手順を実行します。

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

ダイアログボックスフォームのすべての静的ラベルは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialoglabel
```

このクラスは、フォームユーザーインターフェイスのさまざまな場所のテキストに適用できるため、ラベルのサイズや位置の制御には適していません。

**&#x200B; ダイアログボックスラベルのCSS プロパティ。 &#x200B;**

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントの重さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>ラベルのフォントサイズ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>ラベルフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>ラベルのテキストの色： </p> </td> 
  </tr> 
 </tbody> 
</table>

ダイアログボックスラベルはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – すべてのラベルを9つのピクセルフォントを含むグレー、太字に設定するには：

```
.s7ecatalogviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

フォーム入力フィールドの左側に表示されるすべての静的ラベルは、次のように制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputlabel
```

ダイアログボックス入力ラベルの&#x200B;**CSS プロパティ**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>静的ラベルの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> テキスト整列</span> </p> </td> 
   <td colname="col2"> <p>横組みテキストの整列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p>静的ラベルマージン： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>静的なラベルのパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 入力フィールドのラベルを50 ピクセル幅に設定するには、右揃え、パディングを10 ピクセル、右側に10 ピクセルの余白を設定します。

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

各フォーム入力フィールドはコンテナにラップされ、入力フィールドの周囲にカスタムの境界線を適用できます。 これは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer
```

ダイアログボックス入力コンテナの&#x200B;**CSS プロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>入力フィールドコンテナの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>入力フィールドコンテナは、オプションの`state`属性セレクターをサポートしています。 ユーザーが入力データ形式を間違え、インライン検証が失敗した場合は、`verifyerror`に設定されます。 この属性セレクターを使用すると、フォーム内の誤ったユーザー入力を強調表示できます。

ダイアログボックス本文の左端から右端まで広がる入力フィールド（From フィールドとMessage フィールドを含む）のほとんどは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputwide
```

ダイアログボックス入力全体フィールドの&#x200B;**CSS プロパティ**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

「宛先」フィールドは、右側の「メールを削除」ボタンにスペースが割り当てられるので、狭くなります。 これは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputshort
```

ダイアログボックス入力ショートフィールドの&#x200B;**CSS プロパティ**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – すべての入力フィールドの周囲に9 ピクセルのパディングを持つ1 ピクセルのグレーの境界線を持つフォームを設定する。 検証に失敗したフィールドの境界線を赤で表示するには、次の手順を実行します。 フィールドの幅を250 ピクセルにするには、 最後に、残りの入力フィールドは幅300 ピクセルです。

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

メールメッセージ入力フィールドは、次の方法でも制御できます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogmessage
```

このクラスでは、基になる`TEXTAREA`要素に対して特定のプロパティを設定できます。

ダイアログボックスメッセージの&#x200B;**CSS プロパティ**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>メッセージの高さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ワードラップ </span> </p> </td> 
   <td colname="col2"> <p>単語の折り返しスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – メールメッセージの高さを50 ピクセルに設定し、`break-word` ワードラッピングを使用するには、次の手順を実行します。

```
.s7ecatalogviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

「別のメールアドレスを追加」ボタンを使用すると、ユーザーは複数のメールアドレスをメールフォームに追加できます。 これは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton
```

ダイアログボックスの&#x200B;**CSS プロパティ「メールアドレスを追加」ボタン**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>各状態のボタンのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>ボタン領域内のボタン画像の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントの太さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>ボタンのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>ボタンフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行の高さ</span> </p> </td> 
   <td colname="col2"> <p>ボタン内のテキスト高さ。 垂直方向の整列に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> テキスト整列</span> </p> </td> 
   <td colname="col2"> <p>横組みテキストの整列： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 「別の電子メールアドレスを追加」ボタンを25 ピクセルの高さに設定するには、右揃えの12 ポイントの太字フォントと、各状態に異なるテキストカラーと画像を使用します。

```
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

「削除」ボタンを使用すると、ユーザーはメールフォームから追加のアドレスを削除できます。 これは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton
```

ダイアログボックスの&#x200B;**CSS プロパティで電子メールを削除ボタン**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 「削除」ボタンを25 x 25 ピクセルに設定し、状態ごとに異なる画像を使用するには、次の手順を実行します。

```
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

共有されるコンテンツは、ダイアログボックスの本文の下部に表示され、サムネール、タイトル、オリジン URL、説明が含まれます。 これは、次のCSS クラスセレクターで制御されるコンテナにラップされます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**&#x200B; ダイアログボックスのコンテンツ**&#x200B;ージのCSS プロパティ

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>コンテナの境界： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 下のコンテナを設定して、1 ピクセルの点線の境界線を持ち、パディングを持たないようにするには：

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

サムネール画像は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogthumbnail
```

`background-image` プロパティは、コンポーネントロジックによって設定されます。

ダイアログボックスのサムネール画像&#x200B;**CSS プロパティ**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">垂直整列</span> </p> </td> 
   <td colname="col2"> <p>垂直方向の整列サムネール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – サムネールを90 x 60 ピクセルに設定し、パディングの10 ピクセルで上揃えするには、次の手順を実行します。

```
.s7ecatalogviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

コンテンツのタイトル、生成元、説明は、コンテンツサムネールの右側にあるパネルにさらにグループ化されます。 これは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialoginfopanel
```

ダイアログボックス情報パネルの&#x200B;**CSS プロパティ**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>パネルの幅： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンテンツ情報パネルを幅300 ピクセルに設定するには：

```
.s7ecatalogviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

コンテンツタイトルは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogtitle
```

ダイアログボックスのタイトルの&#x200B;**CSS プロパティ**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p>外側のマージン： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 太字フォントを使用し、10 ピクセルの余白を持つようにコンテンツタイトルを設定するには：

```
.s7ecatalogviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

コンテンツのオリジンは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogorigin
```

**&#x200B; ダイアログボックスのコンテンツオリジン**&#x200B;のCSS プロパティ

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p>外側のマージン： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンテンツの原点を10 ピクセルのマージンに設定するには：

```
.s7ecatalogviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

コンテンツの説明は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogdescription
```

ダイアログボックスのコンテンツ説明&#x200B;**CSS プロパティ**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p>外側のマージン： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンテンツの説明を10 ピクセルのマージンで設定し、9 ポイントのフォントを使用するには、次の手順を実行します。

```
.s7ecatalogviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

ユーザーが誤った入力データを入力すると、インライン検証が失敗します。 または、フォームの送信時にダイアログボックスでエラーまたは確認メッセージを表示する必要がある場合は、ダイアログボックス本文の上部にメッセージが表示されます。 これは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage
```

ダイアログボックスの&#x200B;**CSS プロパティに関するエラーメッセージ**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> エラーアイコン。 デフォルトは感嘆符です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> メッセージ領域内のエラーアイコンの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>メッセージのテキストカラー： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行の高さ</span> </p> </td> 
   <td colname="col2"> <p> メッセージ内のテキスト高さ。 垂直方向の整列に影響します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このメッセージは、次の値を持つ`state`属性セレクターをサポートしています：`verifyerror`、`senderror`、および`sendsuccess`。 値`verifyerror`は、インライン入力検証エラーが原因でメッセージが表示される場合に設定されます。 値`senderror`は、バックエンド電子メールサービスでエラーが報告されたときに設定されます。 値`sendsuccess`は、電子メールが正常に送信されたときに設定されます。 これにより、ダイアログボックスの状態に応じてメッセージのスタイルを変更できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 10 ポイントの太字フォントを使用するようにメッセージを設定するには、25 ピクセルの線の高さ、20 ピクセルのパディングを左側に持ち、感嘆符アイコンを使用します。 最後に、エラーが発生した場合は赤いテキスト、成功した場合はアイコンと緑のテキストはありません。

```
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

垂直方向のスクロールが必要な場合は、スクロールバーがダイアログの右端近くのパネルに表示されます。このパネルは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7dialogscrollpanel
```

ダイアログボックススクロールパネルの&#x200B;**CSS プロパティ**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>スクロールパネルの幅： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – スクロールパネルを幅44 ピクセルに設定するには：

```
.s7ecatalogviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

スクロールバー領域の外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar
```

スクロールバーの&#x200B;**CSS プロパティ**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> スクロールバーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p> スクロールパネルの上部から垂直スクロールバーがオフセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p> スクロールパネルの下部から垂直スクロールバーがオフセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p> スクロールパネルの右端から水平スクロールバーがオフセットされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – スクロールパネルの上部、右側、下部から、幅28 ピクセル、8 ピクセルの余白を設定するには、次の手順を実行します。

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

スクロールバートラックは、上と下のスクロールボタンの間の領域です。 コンポーネントは、トラックの位置と高さを自動的に設定します。 トラックは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

スクロール トラックの&#x200B;**CSS プロパティ**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>トラックの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>トラックの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 28 ピクセル幅で灰色の背景を持つスクロールバートラックを設定するには：

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

スクロールバーの親指は、スクロールトラック領域内で垂直方向に移動します。 垂直位置はコンポーネントロジックによって完全に制御されますが、コンテンツの量に応じて親指の高さが動的に変化することはありません。 次のCSS クラスセレクターを使用して、親指の高さやその他の要素を設定できます。

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

スクロールバーの親指の&#x200B;**CSS プロパティ**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>親指の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>親指の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディングトップ </span> </p> </td> 
   <td colname="col2"> <p> トラックの上部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング – 下</span> </p> </td> 
   <td colname="col2"> <p> トラックの下部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>特定のサムステートに対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumbは`state`属性セレクターをサポートしています。このセレクターを使用すると、異なる親指の状態（`up`、`down`、`over`、および`disabled`）に異なるスキンを適用できます。

例 – 28 x 45 ピクセルのスクロールバーの親指を設定するには、上部と下部に10 ピクセルの余白があり、各状態に対して異なるアートワークを設定します。

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

上と下のスクロールボタンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton
```

CSS `top`、`left`、`bottom`、`right`のプロパティを使用してスクロールボタンを配置することはできません。 代わりに、ビューアリジックによって自動的に配置されます。

**上下のスクロールボタンのCSS プロパティ**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>これらのボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態（`up`、`down`、`over`、および`disabled`）に適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 28 x 32 ピクセルで、状態ごとに異なるアートワークを持つスクロールボタンを設定するには：

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

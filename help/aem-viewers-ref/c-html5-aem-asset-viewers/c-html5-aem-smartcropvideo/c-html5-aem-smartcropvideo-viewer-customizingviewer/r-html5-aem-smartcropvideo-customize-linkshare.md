---
title: リンク共有
description: リンク共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティブ化されたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6f2b832f-e627-428a-8673-129bfa58c7e2
TQID: 'https://experienceleague.adobe.com/y9kSFUHZdX5HLf65Zi4K5qRwsX8ghRa2Gj72FSSvzzs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1415
ht-degree: 0%

---

# リンク共有{#link-share}

リンク共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティブ化されたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

リンク共有ボタンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkshare
```

リンク共有ツールの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
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
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

ソーシャル共有パネルからボタンを削除するには、CSS クラスに`display:none` CSS プロパティを設定します。

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)を参照してください。

例 – 28 x 28 ピクセルのリンク共有ボタンを設定し、4つの異なるボタンの状態ごとに異なる画像を表示するには：

```
.s7smartcropvideoviewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

ダイアログボックスがアクティブな場合にweb ページをカバーする背景オーバーレイは、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7backoverlay
```

背景オーバーレイの&#x200B;**CSS プロパティ**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">不透明度</span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイの不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイの色： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 背景オーバーレイを70%の不透明度でグレーに設定するには：

```
.s7smartcropvideoviewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

初期設定では、モーダルダイアログボックスはデスクトップシステムの画面の中央に表示され、タッチデバイスのweb ページ全体を表示します。 いずれの場合も、ダイアログボックスの位置とサイズはコンポーネントによって管理されます。 ダイアログボックスは、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialog
```

ダイアログボックスの&#x200B;**CSS プロパティ**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径（ダイアログボックスでブラウザー全体が使用されない場合）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>ダイアログボックスの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>設定を解除するか、100%に設定する必要があります。この場合、ダイアログボックスはブラウザーウィンドウ全体を使用します（このモードはタッチデバイスで推奨されます）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>設定を解除するか、100%に設定する必要があります。この場合、ダイアログボックスはブラウザーウィンドウ全体を使用します（このモードはタッチデバイスで推奨されます）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ダイアログボックスを設定して、ブラウザーウィンドウ全体を使用し、タッチデバイスの背景が白くなるようにするには、次の手順を実行します。

```
.s7smartcropvideoviewer .s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

ダイアログボックスヘッダーは、アイコン、タイトルテキスト、閉じるボタンで構成されます。 ヘッダーコンテナは

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader
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
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader .s7dialogline
```

ダイアログ行の&#x200B;**CSS プロパティ**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーアイコンとタイトルの内側のパディング </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーアイコンは、次のCSS クラスセレクターで制御されます

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadericon
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダータイトルは、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadertext
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
.s7smartcropvideoviewer .s7linkdialog .s7closebutton
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

閉じるボタンのツールヒントとダイアログボックスのタイトルはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)を参照してください。

例 – パディング、22 x 12 ピクセルのアイコン、太字の16 ポイントのタイトルを含むダイアログボックスヘッダーを設定する。 最後に、28 x 28 ピクセルの「閉じる」ボタンを使用します。このボタンは、ダイアログボックスコンテナの上部から2 ピクセル、右側から2 ピクセルに配置されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

ダイアログフッターは「キャンセル」ボタンで構成されます。 フッターコンテナは、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter
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

フッターには、ボタンを保持する内部コンテナがあります。 これは、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogbuttoncontainer
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

「すべてを選択」ボタンは、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton
```

このボタンは、デスクトップシステムでのみ使用できます。

**すべてを選択ボタンのCSS プロパティ**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
>「すべてを選択」ボタンでは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

キャンセル ボタンは、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton
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

さらに、両方のボタンは共通のCSS クラスを共有します。このクラスには、他のダイアログボックスボタンと同じCSS設定を含めることができます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter .s7button
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

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)を参照してください。

例 – ボタンの状態ごとにテキストの色と背景色が異なる64 x 34 キャンセル ボタンを使用してダイアログボックスフッターを設定するには、次の手順を実行します。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

ヘッダーとフッターの間のメインダイアログ領域には、ダイアログコンテンツが含まれます。 いずれの場合も、コンポーネントはこの領域の幅を管理します。CSSで設定することはできません。 メインダイアログ領域は、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogviewarea
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

例 – メインダイアログボックス領域を300 ピクセルの高さに設定するには、10 ピクセルの余白を設定し、白い背景を使用します。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、で制御されるコンテナ内にあります。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogbody
```

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
.s7smartcropvideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスフォーム内のすべての静的ラベルは

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglabel
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

ダイアログボックスラベルはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)を参照してください。

例 – すべてのラベルを9つのピクセルフォントを持つグレーで太字に設定するには：

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

リンクの上に表示されるテキストコピーのサイズは、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputwide
```

ダイアログボックス入力全体フィールドの&#x200B;**CSS プロパティ**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>テキストの幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – テキストのコピーを幅430 ピクセルで、下部に10 ピクセルのパディングを持つように設定するには：

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

共有リンクはコンテナにラップされ、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputcontainer
```

ダイアログボックス入力コンテナの&#x200B;**CSS プロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>共有リンクコンテナの周りの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 埋め込みコードテキストの周囲に1 ピクセルのグレーの境界線を設定し、パディングが9 ピクセルある場合：

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

共有リンク自体は、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglink
```

ダイアログボックス共有リンクの&#x200B;**CSS プロパティ**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>共有リンクの幅： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 共有リンクを幅450 ピクセルに設定するには：

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```

---
title: 共有を埋め込む
description: 埋め込み共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティブ化されたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 08ba7a29-8b17-4167-a9f3-82aa4cf65556
TQID: 'https://experienceleague.adobe.com/fKaiG7uobh7Bax18dT0aVRcBvNPwwphdxbbs2c36b64'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 2679
ht-degree: 0%

---

# 共有を埋め込む{#embed-share}

埋め込み共有ツールは、ソーシャル共有パネルに追加されたボタンと、ツールがアクティブ化されたときに表示されるモーダルダイアログボックスで構成されます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

埋め込み共有ボタンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embedshare
```

埋め込み共有ツールの&#x200B;**CSS プロパティ**

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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

ソーシャル共有パネルからボタンを削除するには、CSS クラスに`display:none` CSS プロパティを設定します。

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

**例** - 28 x 28 ピクセルの埋め込み共有ボタンを設定し、4つの異なるボタンの状態ごとに異なる画像を表示するには：

```
.s7video360viewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7video360viewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7video360viewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7video360viewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

ダイアログボックスがアクティブな場合にweb ページをカバーする背景オーバーレイは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7backoverlay
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

**例** – 背景オーバーレイを70%の不透明度でグレーに設定するには：

```
.s7video360viewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

初期設定では、モーダルダイアログボックスはデスクトップシステムの画面の中央に表示され、タッチデバイスのweb ページ全体を表示します。 いずれの場合も、ダイアログボックスの位置とサイズはコンポーネントによって管理されます。 ダイアログボックスは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialog
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

**例** - ブラウザーウィンドウ全体を使用し、タッチデバイスで白い背景を持つようにダイアログボックスを設定するには：

```
.s7video360viewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

ダイアログボックスヘッダーは、アイコン、タイトルテキスト、閉じるボタンで構成されます。 ヘッダーコンテナは

```
.s7video360viewer .s7embeddialog .s7dialogheader
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

アイコンとタイトルテキストは、次のように制御される追加のコンテナにラップされます。

```
.s7video360viewer .s7embeddialog .s7dialogheader .s7dialogline
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

ヘッダーアイコンは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialogheadericon
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダータイトルは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialogheadertext
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
.s7video360viewer .s7embeddialog .s7closebutton
```

** 閉じるボタン**のCSS プロパティ

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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

**例** - パディング、24 x 14 ピクセルのアイコン、太字、16 ポイントのタイトルを含むダイアログヘッダーを設定します。 最後に、28 x 28 ピクセルの「閉じる」ボタンを使用して、ダイアログコンテナの上部から2 ピクセル、右側から2 ピクセルを配置します。

```
.s7video360viewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

ダイアログフッターは「キャンセル」ボタンで構成されます。 フッターコンテナは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialogfooter
```

** ダイアログボックスのフッター**のCSS プロパティ

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
.s7video360viewer .s7embeddialog .s7dialogbuttoncontainer
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
.s7video360viewer .s7embeddialog .s7dialogactionbutton
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
.s7video360viewer .s7embeddialog .s7dialogcancelbutton
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
.s7video360viewer .s7embeddialog .s7dialogfooter .s7button
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

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

**例** - 64 x 34 キャンセル ボタンを持つダイアログボックスフッターを設定するには、ボタンの状態ごとに異なるテキスト色と背景色を使用します。

```
.s7video360viewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
```

ヘッダーとフッターの間にあるメインダイアログエリアには、右側のスクロール可能なダイアログコンテンツとスクロールパネルが含まれています。 いずれの場合も、コンポーネントはこの領域の幅を管理しますが、CSSで設定することはできません。 メインダイアログ領域は、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialogviewarea
```

** ダイアログボックスの表示領域のCSS プロパティ **

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

**例** - メインダイアログボックス領域を300 ピクセルの高さに設定するには、10 ピクセルの余白を設定し、白い背景を使用します。

```
.s7video360viewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、次のCSS クラスセレクターで制御されるコンテナ内にあります。

```
.s7video360viewer .s7embeddialog .s7dialogbody
```

このコンテナの高さがメインダイアログボックス領域よりも高いと思われる場合は、コンポーネントによって垂直スクロールが自動的に有効になります。

** ダイアログボックスの本文**のCSS プロパティ

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - 10 ピクセルのパディングを持つようにフォームコンテンツを設定するには：

```
.s7video360viewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスフォーム内のすべての静的ラベルは

```
.s7video360viewer .s7embeddialog .s7dialoglabel
```

このクラスは、フォームユーザーインターフェイスのさまざまな場所のテキストに適用できるため、ラベルのサイズや位置の制御には適していません。

** ダイアログボックスラベルのCSS プロパティ。 **

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

ダイアログボックスラベルはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

**例** – すべてのラベルを9つのピクセルフォントを含むグレーで太字に設定するには：

```
.s7video360viewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

埋め込みコードの上に表示されるテキストコピーのサイズは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialoginputwide
```

ダイアログボックス入力全体フィールドの&#x200B;**CSS プロパティ**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - テキストのコピーを幅430 ピクセル、下に10 ピクセルのパディングを持つように設定するには：

```
.s7video360viewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

埋め込みコードはコンテナにラップされ、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer
```

ダイアログボックス入力コンテナの&#x200B;**CSS プロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードコンテナの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>埋め込みコードコンテナの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 埋め込みコードテキストの周囲に1 ピクセルのグレーの境界線を設定するには、幅430 ピクセル、パディング 10 ピクセルにします。

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

実際の埋め込みコードテキストは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer
```

ダイアログボックス入力コンテナの&#x200B;**CSS プロパティ**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ワードラップ </span> </p> </td> 
   <td colname="col2"> <p>単語の折り返しスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - `break-word` ワードラッピングを使用するように埋め込みコードを設定するには：

```
.s7video360viewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

埋め込みサイズラベルとドロップダウンは、ダイアログボックスの下部にあり、次のCSS クラスセレクターで制御されるコンテナに入れます。

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel
```

ダイアログボックス埋め込みサイズパネルの&#x200B;**CSS プロパティ**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 埋め込みサイズパネルを設定して10 ピクセルのパディングを設定するには：

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

埋め込みサイズラベルのサイズと整列は、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel
```

ダイアログボックス埋め込みサイズパネルの&#x200B;**CSS プロパティ**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">垂直整列</span> </p> </td> 
   <td colname="col2"> <p>垂直方向のラベルの整列： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ラベルの幅： </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 埋め込みサイズラベルを上揃えおよび幅80 ピクセルに設定するには：

```
.s7video360viewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

埋め込みサイズコンボボックスの幅は、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7combobox
```

コンボボックスの&#x200B;**CSS プロパティ**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>コンボボックスの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>コンボボックスでは、`expanded`属性セレクターをサポートしています。使用可能な値は`true`と`false`です。 コンボボックスに事前定義済みの埋め込みサイズの1つが表示されている場合、`true`値が使用されるので、使用可能なすべての幅を使用する必要があります。 `false`値は、コンボボックスでカスタムサイズオプションが選択されている場合に使用されるので、カスタム幅と高さの入力フィールドのスペースを許可するために縮小する必要があります。

**例** – 事前定義済みのアイテムを表示する場合は300 ピクセル、カスタムサイズを表示する場合は110 ピクセルの幅に埋め込みサイズコンボボックスを設定するには、次の手順を実行します。

```
.s7video360viewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7video360viewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

コンボボボックスのテキストの高さは、特殊な内部要素によって定義され、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxtext
```

コンボボボックステキストの&#x200B;**CSS プロパティ**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>コンボボックスのテキストの高さ </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 埋め込みサイズ コンボ ボックスのテキストの高さを40 ピクセルに設定するには：

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

コンボボックスの右側には「ドロップダウン」ボタンがあり、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton
```

コンボボボックスボタンの&#x200B;**CSS プロパティ**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p>コンボボックス内の縦方向ボタンの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>コンボボックス内の水平ボタンの位置。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>各状態のボタン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

**例** - ドロップダウンボタンを28 x 28 ピクセルに設定し、各状態に個別の画像を設定するには：

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

コンボボックスを開いたときに表示される埋め込みサイズのリストを含むパネルは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7comboboxdropdown
```

パネルのサイズと位置は、コンポーネントによって制御されます。 CSSで変更することはできません。

コンボボボックスドロップダウンの&#x200B;**CSS プロパティ**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>パネルの境界線 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - コンボボボックスパネルの境界線を1 ピクセルに設定するには：

```
.s7video360viewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

次のCSS クラスセレクターで制御されるドロップダウンパネル内の1つの項目。

```
.s7video360viewer .s7embeddialog .s7dropdownitemanchor
```

ドロップダウン アイテム アンカーの&#x200B;**CSS プロパティ**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>アイテムの背景： </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - コンボボボックスパネル項目を白い背景に設定するには：

```
.s7video360viewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

次のCSS クラスセレクターで制御されるコンボボボックスパネル内の選択した項目の左側に表示されるチェックマーク。

```
.s7video360viewer .s7embeddialog .s7checkmark
```

チェックマークボックスの&#x200B;**CSS プロパティ**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
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
   <td colname="col2"> <p>アイテム画像： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - チェックマークアイコンを25 x 25 ピクセルに設定するには：

```
.s7video360viewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

「埋め込みサイズ」コンボボックスで「カスタムサイズ」オプションを選択すると、ダイアログボックスの右側に2つの追加の入力フィールドが表示され、ユーザーがカスタム埋め込みサイズを入力できるようになります。 これらのフィールドは、次のCSS クラスセレクターで制御されるコンテナにラップされます。

```
.s7video360viewer .s7embeddialog .s7dialogcustomsizepanel
```

ダイアログボックスのカスタムサイズパネルの&#x200B;**CSS プロパティ**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">さんが</span>を残しました </p> </td> 
   <td colname="col2"> <p> 埋め込みサイズ コンボボックスからの距離。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - カスタムサイズの入力フィールドパネルをコンボボックスの右に20 ピクセルに設定するには：

```
.s7video360viewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

各カスタムサイズ入力フィールドは、境界線をレンダリングし、フィールド間の余白を設定するコンテナで囲まれます。 これは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialogcustomsize
```

ダイアログボックスの&#x200B;**CSS プロパティのカスタムサイズ**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>入力フィールドの周囲にボーダーを設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドマージン。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> 入力フィールドのパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - カスタムサイズの入力フィールドに、1 ピクセルのグレーの境界線、余白、パディングを持ち、幅が70 ピクセルになるように設定するには、次の手順を実行します。

```
.s7video360viewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

垂直方向のスクロールが必要な場合、スクロールバーはダイアログボックスの右端に近いパネルに表示されます。このパネルは、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7dialogscrollpanel
```

ダイアログボックススクロールパネルの&#x200B;**CSS プロパティ**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>スクロールパネルの幅： </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - スクロールパネルを幅44 ピクセルに設定する

```
.s7video360viewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

スクロールバー領域の外観は、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7scrollbar
```

スクロールバーの&#x200B;**CSS プロパティ**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>スクロールバーの幅： </p> </td> 
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

**例** - スクロールパネルの上、右、下から8 ピクセルの余白を持つ幅28 ピクセルのスクロールバーを設定するには、次の手順を実行します。

```
.s7video360viewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

スクロールバートラックは、上と下のスクロールボタンの間の領域です。 コンポーネントは、トラックの位置と高さを自動的に設定します。 トラックは、次のCSS クラスセレクターで制御されます

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

スクロールバートラックの&#x200B;**CSS プロパティ**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>トラック幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 背景色をトラック： </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 幅が28 ピクセル、背景がグレーのスクロールバートラックを設定するには：

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

スクロールバーの親指は、スクロールトラック領域内で垂直方向に移動します。 垂直位置は、コンポーネントロジックによって完全に制御されます。 ただし、コンテンツの量によっては、親指の高さが動的に変化することはありません。 親指の高さやその他の要素は、次のCSS クラスセレクターで設定できます。

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

スクロールバーの親指の&#x200B;**CSS プロパティ**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>親指の幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>親指の高さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディングトップ </span> </p> </td> 
   <td colname="col2"> <p>トラックの上部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング – 下</span> </p> </td> 
   <td colname="col2"> <p> トラックの下部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 特定のサムステートに対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumbは`state`属性セレクターをサポートしています。このセレクターを使用すると、異なる親指の状態（`up`、`down`、`over`、および`disabled`）に異なるスキンを適用できます。

**例** - 28 x 45 ピクセルのスクロールバーの親指を設定するには、上下に10 ピクセルの余白があり、状態ごとにアートワークが異なります。

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

上と下のスクロールボタンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

CSS `top`、`left`、`bottom`、`right`のプロパティを使用してスクロールボタンを配置することはできません。 代わりに、ビューアリジックによって自動的に配置されます。

**上下のスクロールボタンのCSS プロパティ**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>これらのボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態（`up`、`down`、`over`、および`disabled`）に適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

**例** - 28 x 32 ピクセルで、状態ごとに異なるアートワークを持つスクロールボタンを設定するには：

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

---
title: 印刷
description: プリントツールは、コントロールバーに追加されたボタンと、ツールがアクティブ化されたときに表示されるモーダルダイアログボックスで構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 25057e72-f079-4221-91c2-760d99d30633
TQID: 'https://experienceleague.adobe.com/A7cuH0KlQpUIs-0Y-kzgwxRoZmXIcEHqkc-6uae71Kk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1518
ht-degree: 0%

---

# 印刷{#print}

プリントツールは、コントロールバーに追加されたボタンと、ツールがアクティブ化されたときに表示されるモーダルダイアログボックスで構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

プリントボタンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7print
```

印刷ボタンの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーの上部からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> 左の次のボタン、または行の最初のボタンの場合はコントロールバーの左側までの距離。 </p> </td> 
  </tr> 
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 28 x 28 ピクセルの印刷ボタンを設定し、4つの異なるボタンの状態ごとに異なる画像を表示する場合。

```
.s7ecatalogsearchviewer .s7print { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7print[state='up'] { 
background-image:url(images/v2/Print_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7print[state='over'] { 
background-image:url(images/v2/Print_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7print[state='down'] { 
background-image:url(images/v2/Print_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7print[state='disabled'] { 
background-image:url(images/v2/Print_dark_disabled.png); 
}
```

ダイアログボックスがアクティブな場合にweb ページをカバーする背景オーバーレイは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
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
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

デフォルトでは、モーダルダイアログは、デスクトップシステムの画面の中央に表示されます。 ダイアログボックスの位置とサイズは、コンポーネントによって管理されます。 ダイアログは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

ダイアログボックスの&#x200B;**CSS プロパティ**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの背景色 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ダイアログボックスの背景をグレーに設定するには、次の手順を実行します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

ダイアログボックスヘッダーは、アイコン、タイトルテキスト、閉じるボタンで構成されます。 ヘッダーコンテナは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダータイトルは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
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
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

閉じるボタンのツールヒントとダイアログボックスのタイトルはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – パディング、22 x 22 ピクセルのアイコン、太字の16 ポイントタイトルを含むダイアログヘッダーを設定する。 最後に、28 x 28 ピクセルの「閉じる」ボタンを使用して、ダイアログボックスコンテナの上から2 ピクセル、右から2 ピクセルの位置に配置します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgprint_cap.png"); 
    height: 22px; 
    width: 22px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

ダイアログボックスフッターは、「キャンセル」ボタンと「プリントに送信」ボタンで構成されます。 フッターコンテナは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
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

フッターには、両方のボタンを保持するインナーコンテナがあります。 これは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
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

「印刷に送信」ボタンは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
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

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 64 x 34 キャンセル ボタンと96 x 34 プリントに送信ボタンを持つダイアログボックスフッターを設定するには、ボタンの状態ごとにテキストの色と背景色が異なります。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton { 
 width:96px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

ヘッダーとフッターの間のメインダイアログ領域には、ダイアログコンテンツが含まれます。 いずれの場合も、コンポーネントはこの領域の幅を管理しますが、CSSで設定することはできません。 メインダイアログ領域は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

** ダイアログボックスの表示領域のCSS プロパティ **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p> メインダイアログボックス領域の高さ。 </p> </td> 
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

例 – メインダイアログ領域の高さを自動計算し、10 ピクセルのマージンを設定し、白い背景を使用するには、次の手順を実行します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、次のCSS クラスセレクターで制御されるコンテナ内にあります。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
```

** ダイアログボックスの本文**のCSS プロパティ

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
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスフォームは行ごとに入力されます。各行には、フォームコンテンツの一部（ラベルやテキスト入力フィールドなど）が含まれます。 単一のフォーム行は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

ダイアログコンテンツのブロックのサイズは、次のCSS クラスセレクターで制御されます。

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

ダイアログ入力幅の&#x200B;**CSS プロパティ**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ブロック幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>行の内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンテンツブロックを幅430 ピクセル、下に10 ピクセルのパディングを持つように設定するには：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

ダイアログボックスフォームのすべての静的ラベルは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
```

このクラスは、フォームユーザーインターフェイスの様々な場所のテキストに適用できるため、ラベルのサイズや位置の制御には適していません。

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

ダイアログボックスラベルはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – すべてのラベルを9つのピクセルフォントを含むグレー、太字に設定するには：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

入力コントロールはコンテナにラップされ、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

ダイアログボックス入力コンテナの&#x200B;**CSS プロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング左</span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ダイアログボックスの左端から30 ピクセルのパディングを設定します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

ラジオボタンとそのキャプションテキストは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

ダイアログボックスオプションの&#x200B;**CSS プロパティ**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> キャプション付きのラジオボタンの幅の合計。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>キャプションテキストの色： </p> </td> 
  </tr> 
 </tbody> 
</table>

ラジオボタンとそのキャプションの間の間隔は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

ダイアログボックスオプション入力&#x200B;**の** CSS プロパティ

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右余白</span> </p> </td> 
   <td colname="col2"> <p> ラジオボタンとキャプションの間の間隔。 </p> </td> 
  </tr> 
 </tbody> 
</table>

印刷範囲を選択するための数値ピッカーは、次のCSS クラスセレクターで制御されます

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

ダイアログボックスの印刷範囲&#x200B;**CSS プロパティ**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> 数値ピッカーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p> 数値ピッカーの周囲の間隔。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – すべてのラジオボタンを、黒いテキスト、10 ピクセルの間隔、42 ピクセルの幅の数値ピッカーで150 ピクセル幅に設定するには、次の手順を実行します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption { 
    color: #000000; 
    width: 150px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption input { 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange { 
    margin-left: 10px; 
    margin-right: 10px; 
    width: 42px; 
}
```

ページ範囲の選択と印刷レイアウトセクションの間の水平方向の区切り線は、次のCSS クラスセレクターで制御されます。

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**水平分割線のCSS プロパティ**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p> 区切り線を囲む。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>インナーパディング： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>区切り線の幅： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p>外側の余白 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 430 ピクセル幅のグレーディバイダを設定するには、両側に10 ピクセルの垂直方向のパディング、上部に10 ピクセルのマージンを設定します。

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```

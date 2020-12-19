---
description: プリントツールは、コントロールバーに追加されるボタンと、ツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。
seo-description: プリントツールは、コントロールバーに追加されるボタンと、ツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。
seo-title: 印刷
solution: Experience Manager
title: 印刷
topic: Dynamic media
uuid: 7be047d8-d1be-4bda-90ca-6b55c749cc64
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1493'
ht-degree: 2%

---


# 印刷{#print}

プリントツールは、コントロールバーに追加されるボタンと、ツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

プリントボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7print
```

**プリントボタンのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーの上端からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> 左側の次のボタンまでの距離、または行の最初のボタンの場合はコントロールバーの左側までの距離です。 </p> </td> 
  </tr> 
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
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 28 x 28ピクセルで、ボタンの4つの状態ごとに異なる画像を表示する印刷ボタンを設定するには、次のように記述します。

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

ダイアログボックスがアクティブなときのWebページをカバーする背景オーバーレイは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
```

**背面オーバーレイのCSSプロパティ**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacity  </span> </p> </td> 
   <td colname="col2"> <p> 背景オーバーレイの不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>背景オーバーレイのカラー </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 不透明度70 %のグレーの背景オーバーレイを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

デフォルトでは、モーダルダイアログはデスクトップシステムの画面の中央に表示されます。 ダイアログボックスの位置とサイズは、コンポーネントで管理します。このダイアログは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**ダイアログボックスのCSSプロパティ**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの背景色； </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — グレーの背景を持つダイアログボックスを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

ダイアログボックスのヘッダーは、アイコン、タイトルテキストおよび閉じるボタンで構成されます。 ヘッダーのコンテナは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
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

アイコンとタイトルテキストは、追加のコンテナにまとめられます。以下を使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
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

ヘッダーのアイコンは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
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
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのタイトルは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
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
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
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
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

「閉じる」ボタンのツールチップとダイアログボックスのタイトルをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — パディング、22 x 22ピクセルのアイコン、太字の16ポイントのタイトルおよび28 x 28ピクセルの閉じるボタンを設定し、ダイアログボックスのコンテナの上から2ピクセル、右から2ピクセルの位置に配置するには、次のように記述します。

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

ダイアログボックスのフッターは、「キャンセル」ボタンと「印刷に送信」ボタンで構成されます。 フッターのコンテナは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
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

フッターには、両方のボタンを保持する内側のコンテナがあります。 これは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
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

「キャンセル」ボタンは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
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
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

「印刷に送信」ボタンは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**ダイアログボックスのアクションボタンのCSSプロパティ**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
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

ボタンのツールヒントをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — 64 x 34の「キャンセル」ボタンと96 x 34の「印刷に送信」ボタンを含み、テキスト色と背景色がボタンの状態ごとに異なるダイアログボックスフッターを設定するには、次のように記述します。

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

ダイアログのメイン領域（ヘッダーとフッターの間）には、ダイアログのコンテンツが含まれます。 どのような場合でも、コンポーネントがこの領域の幅を管理するので、CSSで設定することはできません。 ダイアログのメイン領域は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**ダイアログボックスの表示領域のCSSプロパティ**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスのメイン領域の高さ。 </p> </td> 
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

例 — 高さが自動的に計算され、マージンが10ピクセルで、白の背景を使用するダイアログのメイン領域を設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、コンテナ内に配置します。このコンテンツは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスのフォームは1行ずつ入力されます。各行は、フォームコンテンツの一部（ラベルやテキスト入力フィールドなど）を担います。 フォームの1行は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**ダイアログボックスの行のCSSプロパティ**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>行の内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 各行に10ピクセルのパディングがあるダイアログボックスのフォームを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

ダイアログコンテンツのブロックのサイズは、以下のCSSクラスセレクターを使用して制御します。

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**ダイアログの入力幅のCSSプロパティ**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>ブロックの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>行の内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が430ピクセルで、下部に10ピクセルのパディングがあるコンテンツブロックを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

ダイアログボックスのフォーム内の静的なラベルはすべて、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
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

ダイアログボックスのラベルをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — グレー、太字、9ピクセルのフォントとなるようにすべてのラベルを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

入力コントロールはコンテナにまとめられ、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**ダイアログボックスの入力コンテナのCSSプロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left  </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — ダイアログボックスの左端から30ピクセルのパディングを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

ラジオボタンとそのキャプションテキストは、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**ダイアログボックスオプションのCSSプロパティ**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> キャプションを含むラジオボタンの合計の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>キャプションのテキストカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ラジオボタンとそのキャプションの間隔は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**ダイアログボックスのオプション入力のCSSプロパティ**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right  </span> </p> </td> 
   <td colname="col2"> <p> ラジオボタンとキャプションの間隔。 </p> </td> 
  </tr> 
 </tbody> 
</table>

印刷範囲選択の数値ピッカーは、以下のCSSクラスセレクターを使用して制御します

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**ダイアログボックスのプリント範囲のCSSプロパティ**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> 数値ピッカーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p> 数値ピッカーの周囲の間隔。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が150ピクセルで、黒のテキスト、10ピクセルの間隔、幅が42ピクセルの数値ピッカーを使用するすべてのラジオボタンを設定するには、次のように記述します。

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

ページ範囲選択と印刷レイアウトセクションの水平区切りは、以下のCSSクラスセレクターを使用して制御します。

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**水平区切りのCSSプロパティ**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p> 区切りの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>区切りの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>外側の余白 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が430ピクセルで、両側に10ピクセルの垂直パディングがあり、上部に10ピクセルのマージンがあるグレーの区切りを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```


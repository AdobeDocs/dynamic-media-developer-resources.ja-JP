---
title: 印刷
description: 印刷ツールは、コントロールバーに追加されるボタンと、ツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c5939cdc-fa4e-4f19-b2a9-21b389492c4f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 2%

---

# 印刷{#print}

印刷ツールは、コントロールバーに追加されるボタンと、ツールがアクティブになったときに表示されるモーダルダイアログボックスで構成されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

印刷ボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7print
```

**印刷ボタンの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーの上からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> 左側の次のボタンまたはこのボタンが連続する最初のボタンの場合はコントロールバーの左側への距離。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 28 x 28 ピクセルで、ボタンの 4 つの状態ごとに異なる画像を表示する印刷ボタンを設定するには、次のように記述します。

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

ダイアログボックスがアクティブなときに Web ページを覆う背景オーバーレイは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
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
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

デフォルトでは、モーダルダイアログはデスクトップシステムの画面の中央に表示されます。 ダイアログボックスの位置とサイズは、コンポーネントによって管理されます。 ダイアログは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**ダイアログボックスの CSS プロパティ**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスの背景色 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — グレーの背景を持つダイアログボックスを設定するには：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

ダイアログボックスのヘッダーは、アイコン、タイトルテキストおよび閉じるボタンで構成されます。 ヘッダーコンテナは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
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

アイコンとタイトルテキストは、以下の方法で制御できる追加のコンテナにまとめられます。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
```

**ダイアログの行の CSS プロパティ**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p> ヘッダーアイコンとタイトルの内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのアイコンは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
```

**ダイアログボックスヘッダーのアイコンの CSS プロパティ**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>アイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>アイコンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>アイコン画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

ヘッダーのタイトルは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
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
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

「閉じる」ボタンのツールチップとダイアログボックスのタイトルは、ローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — パディング、22 x 22 ピクセルのアイコン、太字の 16 ポイントのタイトルを含むダイアログヘッダーを設定するには、次のように記述します。 最後に、28 x 28 ピクセルの「閉じる」ボタンを使用して、ダイアログボックスコンテナの上から 2 ピクセル、右から 2 ピクセルの位置に配置します。

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

ダイアログボックスのフッターは、「キャンセル」ボタンと「印刷に送信」ボタンで構成されます。 フッターコンテナは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
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
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
```

**ダイアログボックスの「キャンセル」ボタンの CSS プロパティ**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
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

「印刷に送信」ボタンは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**ダイアログボックスのアクションボタンの CSS プロパティ**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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

また、両方のボタンは、他のダイアログボックスのボタンと同じ CSS 設定を含むことができる、共通の CSS クラスを共有します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
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

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 64 x 34 の「キャンセル」ボタンと 96 x 34 の「印刷に送信」ボタンを含むダイアログボックスフッターを設定し、テキストの色と背景色をボタンの状態ごとに異なるようにするには、次のように記述します。

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

メインダイアログ領域（ヘッダーとフッターの間）には、ダイアログのコンテンツが含まれます。 どのような場合でも、コンポーネントがこの領域の幅を管理するので、CSS で設定することはできません。 ダイアログのメイン領域は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**ダイアログボックス表示領域の CSS プロパティ**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> ダイアログボックスのメイン領域の高さです。 </p> </td> 
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

例 — 高さが自動的に計算され、マージンが 10 ピクセルで、白の背景を使用するダイアログ領域を設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

すべてのフォームコンテンツ（ラベルや入力フィールドなど）は、コンテナ内に配置され、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
```

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
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

ダイアログボックスのフォームは 1 行ごとに入力され、各行はフォームコンテンツの一部（ラベルやテキスト入力フィールドなど）を保持します。 単一のフォーム行は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

ダイアログコンテンツのブロックのサイズは、以下の CSS クラスセレクターを使用して制御します。

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**ダイアログ入力の幅の CSS プロパティ**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ブロック幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側の行のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 430 ピクセルで、下部に 10 ピクセルのパディングがあるコンテンツブロックを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

ダイアログボックスフォーム内のすべての静的ラベルは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
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
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>ラベルのテキストの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ダイアログボックスのラベルはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — グレー、太字、9 ピクセルのフォントとなるすべてのラベルを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

入力コントロールはコンテナにまとめられ、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**ダイアログボックスの入力コンテナの CSS プロパティ**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — ダイアログボックスの左端から 30 ピクセルのパディングを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

ラジオボタンとそのキャプションテキストは、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**ダイアログボックスオプションの CSS プロパティ**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> キャプションを含むラジオボタンの合計の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>キャプションのテキストカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ラジオボタンとキャプションの間隔は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**ダイアログボックスオプション入力の CSS プロパティ**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p> ラジオボタンとキャプションの間の間隔。 </p> </td> 
  </tr> 
 </tbody> 
</table>

印刷範囲選択の数値選択は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**ダイアログボックスの印刷範囲の CSS プロパティ**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 数値ピッカーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 数値ピッカーの周囲の間隔。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 150 ピクセルで、黒いテキスト、10 ピクセルの間隔、幅が 42 ピクセルの数値選択機能を持つラジオボタンをすべて設定するには、次のように記述します。

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

ページ範囲選択と印刷レイアウトセクションの間の水平方向の区切りは、以下の CSS クラスセレクターを使用して制御します。

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**水平ディバイダの CSS プロパティ**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p> ディバイダの周りの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ディバイダの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外側の余白 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 両側に 10 ピクセルの垂直パディングを持ち、上部に 10 ピクセルのマージンを持つ、430 ピクセル幅のグレーディバイダを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```

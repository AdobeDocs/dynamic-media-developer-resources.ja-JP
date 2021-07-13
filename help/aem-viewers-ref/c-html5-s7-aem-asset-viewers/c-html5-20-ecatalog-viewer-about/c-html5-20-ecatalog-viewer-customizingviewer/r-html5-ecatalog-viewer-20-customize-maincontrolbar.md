---
description: メインコントロールバーは、デスクトップシステムおよびタブレットの矩形の領域で、eCatalogビューアで使用できるすべてのユーザーインターフェイスコントロール（大きいページボタンを除く）が含まれます。
solution: Experience Manager
title: メインコントロールバー
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,User
exl-id: 4db16599-ede0-47ae-bb5a-840655d3620b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 1%

---

# メインコントロールバー{#main-control-bar}

メインコントロールバーは、デスクトップシステムおよびタブレットの矩形の領域で、eCatalogビューアで使用できるすべてのユーザーインターフェイスコントロール（大きいページボタンを除く）が含まれます。

携帯電話では、「サムネール」、「目次」、「ダウンロード」、「印刷」、「お気に入り」、「ソーシャル共有」、「全画面表示」および「閉じる」の各ボタンが保持されます。 ただし、最初のページボタンと最後のページボタンおよびページインジケーターは、メインコントロールバーから削除され、代わりにセカンダリコントロールバーに追加されます。 デフォルトでは、メインコントロールバーはデスクトップシステムおよび携帯電話ではビューア領域の上部に表示され、タブレットではビューア領域の下部に移動します。 常に、ビューアの幅全体を使用できます。 CSS内での、ビューアのコンテナに対するカラー、高さ、垂直方向の位置を変更できます。

メインコントロールバーの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>ビューアの上端からの位置 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビューアの下端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — 高さが36ピクセルで、ビューアのコンテナの上に配置するグレーのメインコントロールバーを設定します。

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

メインコントロールバーは、オプションのスクロール機能をサポートしています。 ビューアの幅が小さすぎて、コントロールバーのすべてのボタンプリセットに収まる十分なスペースがない場合にアクティブになります。 この場合、コントロールバーの右側に2つの状態の矢印ボタンが表示されます。 このボタンをクリックまたはタップすると、スクロールボタンの状態に応じて、すべてのコントロールバー要素が左または右にスクロールします。 この機能の主な使用例は、縦長の画面が小さいモバイルデバイスです。

スクロール機能は、メインコントロールバーに対して有効になり、セカンダリコントロールバーに対しては無効になります。 この機能は、次のCSSクラスセレクターを使用してオン/オフを切り替えます。

`.s7ecatalogviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> static </span>に設定すると、スクロール機能は無効になります。 </p> <p>このプロパティを<span class="codeph">絶対</span>に設定すると、スクロール機能が有効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

スクロールボタンは、ボタンを適切に配置する特殊なコンテナ要素に追加されます。スクロールボタンの高さがコントロールバーの高さより小さい場合は、コントロールバーの背景の他の部分とは異なるスタイルでボタンの周囲の領域を設定できます。

このスクロールボタンコンテナの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>通常は、スクロールボタン自体の幅と等しいか、またはそれより大きい値を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>コンテナの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSSを使用して、スクロールボタン自体のサイズを設定し、スキンを設定することができます。

このボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターと`selected`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に、`state="selected"`は、コントロールバーの内容を左にスクロール可能な場合の初期スクロールボタンの状態に対応します。`state="default"`は、コンテンツが左端までスクロールされた状態に対応し、スクロールボタンは、コンテンツを初期状態に戻すよう提案します。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

**例**  — 携帯電話のメインコントロールバーでスクロール機能を有効にし、選択時または未選択時の4つのボタンの状態ごとに異なる画像を表示する64 x 64ピクセルのスクロールボタンを設定します。

```
.s7ecatalogviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```

---
description: メインコントロールバーは、デスクトップシステムおよびタブレットでは長方形の領域で、eCatalogビューアで使用できるすべてのユーザインターフェイスコントロール（大きいページボタンを除く）が含まれています。
seo-description: メインコントロールバーは、デスクトップシステムおよびタブレットでは長方形の領域で、eCatalogビューアで使用できるすべてのユーザインターフェイスコントロール（大きいページボタンを除く）が含まれています。
seo-title: メインコントロールバー
solution: Experience Manager
title: メインコントロールバー
topic: Dynamic media
uuid: 0900f678-d7ec-4653-bc8a-21b8da7d5044
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# メインコントロールバー{#main-control-bar}

メインコントロールバーは、デスクトップシステムおよびタブレットでは長方形の領域で、eCatalogビューアで使用できるすべてのユーザインターフェイスコントロール（大きいページボタンを除く）が含まれています。

携帯電話では、サムネール、目次、ダウンロード、印刷、お気に入り、ソーシャルシェア、フルスクリーン、閉じるボタンが維持されます。 ただし、最初のページボタンと最後のページボタン、ページインジケーターはメインコントロールバーから削除され、代わりにセカンダリコントロールバーに追加されます。 デフォルトでは、メインコントロールバーはデスクトップシステムおよび携帯電話ではビューア領域の上部に表示され、タブレットではビューア領域の下部に移動されます。 ビューアの幅は常に使用可能な幅全体になります。 CSS内での、ビューアのコンテナに対するカラー、高さおよび垂直方向の位置を変更できます。

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
   <td colname="col2"> <p>ビューアの上端からの位置。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** — 高さが36ピクセルで、ビューアのコンテナの上に配置するグレーのメインコントロールバーを設定します。

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

メインコントロールバーでは、オプションのスクロール機能がサポートされています。 ビューアの幅が小さすぎて、コントロールバーのすべてのボタンプリセットに収まるスペースがない場合にアクティブになります。 この場合、コントロールバーの右側に2つの状態を持つ矢印ボタンが表示されます。 このボタンをクリックまたはタップすると、スクロールボタンの状態に応じて、すべてのコントロールバー要素が左または右にスクロールします。 この機能の主な使用例は、縦長の画面が小さいモバイルデバイスです。

スクロール機能は、メインコントロールバーに対して有効になり、セカンダリコントロールバーに対しては無効になります。 この機能は、以下のCSSクラスセレクターを使用してオン/オフにします。

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
   <td colname="col1"> <p> <span class="codeph"> 掲載順位 </span> </p> </td> 
   <td colname="col2"> <p>staticに設定すると、ス <span class="codeph"> クロー </span> ル機能は無効になります。 </p> <p>このプロパティをabsoluteに設定す <span class="codeph"> ると、ス </span> クロール機能が有効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

スクロールボタンを特別なコンテナ要素に追加し、ボタンの位置を適切に決め、スクロールボタンの高さがコントロールバーの高さよりも小さい場合に備えて、コントロールバーの背景の他の領域とは異なるスタイルを設定できます。

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
   <td colname="col2"> <p>通常は、スクロールボタン自体の幅と同じか、それより大きい値を指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>コンテナの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

スクロールボタン自体のサイズ設定とスキン表示は、CSSを使用して行うことができます。

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>特定のボタンの状態で表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p>CSSスプライトも参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 照してくださ </a>い。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、属性セレ `state` クターと `selected` 属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に、は、コン `state="selected"` トロールバーの内容を左にスクロールできる場合のスクロールボタンの初期状態に対応します。コンテ `state="default"` ンツを左端までスクロールした場合の状態に対応し、スクロールボタンを押すと初期状態に戻ります。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザインターフェイス要素のローカリゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

**例** — 携帯電話のメインコントロールバーでスクロール機能を有効にし、選択時または未選択時のボタンの4つの状態ごとに異なる画像を表示する64 x 64ピクセルのスクロールボタンを設定します。

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


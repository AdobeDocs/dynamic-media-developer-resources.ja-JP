---
title: メインコントロールバー
description: メインコントロールバーは、デスクトップシステムおよびタブレットの長方形の領域で、eCatalog ビューアで使用できるすべてのユーザーインターフェイスコントロール（大きいページボタンを除く）が含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 4db16599-ede0-47ae-bb5a-840655d3620b
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 1%

---

# メインコントロールバー{#main-control-bar}

メインコントロールバーは、デスクトップシステムおよびタブレットの長方形の領域で、eCatalog ビューアで使用できるすべてのユーザーインターフェイスコントロール（大きいページボタンを除く）が含まれます。

携帯電話では、引き続き「サムネール」、「目次」、「ダウンロード」、「印刷」、「お気に入り」、「ソーシャル共有」、「全画面表示」および「閉じる」ボタンが保持されます。 ただし、最初のページボタンと最後のページボタンおよびページインジケーターは、メインコントロールバーから削除され、代わりにセカンダリコントロールバーに追加されます。 デフォルトでは、メインコントロールバーはデスクトップシステムおよび携帯電話ではビューア領域の上部に表示され、タブレットではビューア領域の下部に移動します。 ビューアの幅は常に、使用可能な全体になります。 CSS 内で、ビューアのコンテナを基準にして、カラー、高さ、垂直方向の位置を変更できます。

メインコントロールバーの外観は、以下の CSS クラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>ビューアの上部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビューアの下部からの位置。 </p> </td> 
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

**例**  — 高さが 36 ピクセルで、ビューアのコンテナの上に配置するグレーのメインコントロールバーを設定します。

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

メインコントロールバーでは、オプションのスクロール機能がサポートされています。 ビューアの幅が小さすぎて、コントロールバーにプリセットされているすべてのボタンに収まるのに十分なスペースがない場合に、このアクティベートが有効になります。 この場合、コントロールバーの右側に 2 つの状態の矢印ボタンが表示されます。 このボタンをクリックまたはタップすると、スクロールボタンの状態に応じて、すべてのコントロールバー要素を左または右にスクロールします。 この機能の主な使用例は、小さい画面を縦向きで使用するモバイルデバイスです。

スクロール機能は、メインコントロールバーに対して有効で、セカンダリコントロールバーに対しては無効です。 この機能は、次の CSS クラスセレクターを使用してオン/オフを切り替えます。

`.s7ecatalogviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position </span> </p> </td> 
   <td colname="col2"> <p>に設定する場合 <span class="codeph"> 静的 </span> スクロール機能は無効です。 </p> <p>このプロパティをに設定します。 <span class="codeph"> 絶対 </span> をクリックして、スクロール機能を有効にします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

スクロールボタンは、ボタンを適切に配置する特別なコンテナ要素に追加されます。 スクロールボタンの高さがコントロールバーの高さより小さい場合に、コントロールバーの背景の他の部分とは異なるスタイルでボタンの周囲の領域を設定できます。

このスクロールボタンコンテナの外観は、以下の CSS クラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>通常は、スクロールボタン自体の幅と等しいか、それより大きい値を設定する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>コンテナの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS を使用して、スクロールボタン自体のサイズを設定したり、スキンを設定したりできます。

このボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

`.s7ecatalogviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
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
   <td colname="col2"> <p>CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` および `selected` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に `state="selected"` は、コントロールバーの内容を左にスクロールできる場合の、最初のスクロールボタンの状態に対応します。 属性 `state="default"` は、コンテンツが左端までスクロールされた状態に対応し、スクロールボタンは、コンテンツを初期状態に戻すことを示します。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

**例**  — 携帯電話のメインコントロールバーでスクロール機能を有効にするには また、64 x 64 ピクセルで、選択時または未選択時の 4 つのボタンの状態ごとに異なる画像を表示するスクロールボタンを設定します。

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

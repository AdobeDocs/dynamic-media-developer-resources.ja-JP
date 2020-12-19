---
description: メインコントロールバーは、デスクトップシステムおよびタブレットの矩形の領域で、eCatalog検索ビューアで使用できるすべてのユーザインターフェイスコントロール（大きいページボタンを除く）が含まれます。
seo-description: メインコントロールバーは、デスクトップシステムおよびタブレットの矩形の領域で、eCatalog検索ビューアで使用できるすべてのユーザインターフェイスコントロール（大きいページボタンを除く）が含まれます。
seo-title: メインコントロールバー
solution: Experience Manager
title: メインコントロールバー
topic: Dynamic media
uuid: 21b6e6cd-115f-4c7b-a61e-34b307142045
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 1%

---


# メインコントロールバー{#main-control-bar}

メインコントロールバーは、デスクトップシステムおよびタブレットの矩形の領域で、eCatalog検索ビューアで使用できるすべてのユーザインターフェイスコントロール（大きいページボタンを除く）が含まれます。

携帯電話では、サムネール、目次、ダウンロード、印刷、お気に入り、ソーシャルシェア、フルスクリーン、閉じるボタンが保持されます。 ただし、最初のページボタン、最後のページボタン、ページインジケーターは、メインコントロールバーから削除され、代わりにセカンダリコントロールバーに追加されます。 デフォルトでは、メインコントロールバーはデスクトップシステムおよび携帯電話ではビューア領域の上部に表示され、タブレットではビューア領域の下部に移動されます。 常に、ビューアの幅いっぱいに表示されます。 CSS内での、ビューアのコンテナに対するカラー、高さおよび垂直方向の位置を変更できます。

メインコントロールバーの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogsearchviewer .s7controlbar`

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — 高さが36ピクセルで、ビューアコンテナの上部に配置するグレーのメインコントロールバーを設定します。

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

メインコントロールバーでは、オプションのスクロール機能がサポートされています。 ビューアの幅が小さすぎて、コントロールバーのすべてのボタンプリセットに収まるスペースがない場合は、アクティブになります。 この場合、コントロールバーの右側に2つの状態を持つ矢印ボタンが表示されます。 このボタンをクリックまたはタップすると、スクロールボタンの状態に応じて、すべてのコントロールバー要素が左または右にスクロールします。 この機能の主な使用例は、縦長の小さい画面を持つモバイルデバイスです。

スクロール機能は、メインコントロールバーに対して有効になり、セカンダリコントロールバーに対しては無効になります。 この機能のオン/オフは、以下のCSSクラスセレクターを使用して切り替えます。

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

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

特別なコンテナ要素にスクロールボタンを追加しました。この要素を使用すると、ボタンの位置を適切に決め、スクロールボタンの高さがコントロールバーの高さよりも小さい場合に、コントロールバーの背景の他の部分とは異なるスタイルを設定できます。

このスクロールボタンコンテナの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

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
   <td colname="col2"> <p>通常は、スクロールボタン自体の幅と同じかそれ以上にする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>コンテナの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

スクロールボタン自体のサイズ設定とスキン設定は、CSSを使用して行うことができます。

このボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

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
   <td colname="col2"> <p>ボタンの特定の状態に対して表示する画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`および`selected`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に、`state="selected"`は、コントロールバーの内容を左にスクロールできる場合の初期スクロールボタンの状態に対応します。`state="default"`は、コンテンツを左端までスクロールしたときの状態に対応し、スクロールボタンからは初期状態に戻すように指示されます。

ボタンのツールチップをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

**例**  — 携帯電話のメインコントロールバーのスクロール機能を有効にし、選択時または未選択時のボタンの4つの状態ごとに異なる画像を表示する64 x 64ピクセルのスクロールボタンを設定します。

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```


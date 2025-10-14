---
title: メインコントロールバー
description: メイン コントロール バーは、デスクトップ システムおよびタブレット上の四角形の領域で、eCatalog ビューアで使用可能なすべてのユーザ インタフェース コントロール（[ 大きなページ ] ボタンを除く）が含まれています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 4db16599-ede0-47ae-bb5a-840655d3620b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# メインコントロールバー{#main-control-bar}

メイン コントロール バーは、デスクトップ システムおよびタブレット上の四角形の領域で、eCatalog ビューアで使用可能なすべてのユーザ インタフェース コントロール（[ 大きなページ ] ボタンを除く）が含まれています。

携帯電話では、サムネール、目次、ダウンロード、印刷、お気に入り、ソーシャル共有、全画面表示、閉じるボタンが保持されます。 ただし、メイン コントロール バーから [ 最初のページ ] ボタンと [ 最後のページ ] ボタン、およびページ インジケータは削除され、代わりにセカンダリ コントロール バーに追加されます。 デフォルトでは、メインコントロールバーはデスクトップシステムや携帯電話のビューアエリアの上部に表示され、タブレットのビューアエリアの下部に移動します。 常に、使用可能なビューアの幅全体を使用します。 ビューアのコンテナを基準にして、CSS でカラー、高さ、垂直方向の位置を変更できます。

メインコントロールバーの外観は、次の CSS クラスセレクターで制御します。

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
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>ビューアの上部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビューアの下部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>メイン コントロール バーの高さです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>メイン コントロール バーの背景色です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 高さが 36 ピクセルで、ビューアコンテナの上部に配置されるグレーのメインコントロールバーを設定します。

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

メインコントロールバーは、オプションのスクロール機能をサポートしています。 このオプションは、ビューアの幅が小さすぎて、コントロールバーにプリセットされたすべてのボタンを収めるだけのスペースがない場合にアクティブになります。 この場合は、コントロールバーの右側に 2 つの状態の矢印ボタンが表示されます。 このボタンをクリックまたはタップすると、スクロールボタンの状態に応じて、すべてのコントロールバー要素が左または右にスクロールします。 この機能の主なユースケースは、縦向きの小さな画面を持つモバイルデバイスです。

スクロール機能はメインコントロールバーで有効になり、セカンダリコントロールバーでは無効になります。 この機能は、次の CSS クラスセレクターを使用してオン/オフを切り替えます。

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
   <td colname="col2"> <p>静的に設定すると <span class="codeph"> スクロール機能 </span> 無効になります。 </p> <p>このプロパティを絶対 <span class="codeph"> に設定 </span> てスクロール機能を有効にします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

スクロールボタンは、ボタンを適切に配置する特別なコンテナ要素に追加されます。 スクロールボタンの高さがコントロールバーの高さより小さい場合に、ボタンの周囲の領域を他のコントロールバーの背景とは異なるスタイルで表示できます。

このスクロールボタンコンテナの外観は、次の CSS クラスセレクターで制御します。

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
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>通常は、スクロールボタン自体の幅と同じか、それよりも大きい値を指定する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>コンテナの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS を使用して、スクロールボタン自体のサイズを設定したりスキンを作成したりできます。

このボタンの外観は、次の CSS クラスセレクターで制御します。

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
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> ール </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state` および `selected` 属性セレクターをサポートしており、異なるボタン状態に異なるスキンを適用するために使用できます。 特に、コントロールバー `state="selected"` 内容を左にスクロールできる場合は、最初のスクロールボタンの状態に対応します。 属性 `state="default"` は、コンテンツが左側にスクロールされ、スクロールボタンによって初期状態に戻された場合の状態に対応します。

ボタンのツールチップはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

**例** – 携帯電話用のメインコントロールバーのスクロール機能を有効にします。 次のように、選択または未選択の場合に 4 つの異なるボタン状態ごとに異なる画像を表示する、64 x 64 ピクセルのスクロールボタンを設定します。

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

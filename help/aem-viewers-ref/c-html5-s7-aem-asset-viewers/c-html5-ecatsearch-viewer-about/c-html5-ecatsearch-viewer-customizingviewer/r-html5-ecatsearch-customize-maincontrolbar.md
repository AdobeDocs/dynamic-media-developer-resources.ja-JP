---
title: メインコントロールバー
description: メインコントロールバーは、デスクトップシステムおよびタブレット上の長方形の領域で、eCatalog Search ビューアで使用できるすべてのユーザーインターフェイスコントロール（大きなページボタンを除く）が含まれています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cee6a4d4-4099-4bc8-9d67-00a1e963a139
TQID: 'https://experienceleague.adobe.com/rZIWgDCOWs2uXZ2uAKMrUnlmF4JcH6IOd5-kcECC-jE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 0%

---

# メインコントロールバー{#main-control-bar}

メインコントロールバーは、デスクトップシステムおよびタブレット上の長方形の領域で、eCatalog Search ビューアで使用できるすべてのユーザーインターフェイスコントロール（大きなページボタンを除く）が含まれています。

携帯電話では、サムネール、目次、ダウンロード、印刷、お気に入り、ソーシャル共有、フルスクリーン、閉じるボタンが引き続き保持されます。 ただし、最初のページと最後のページのボタン、およびページインジケーターは、メインコントロールバーから削除され、代わりにセカンダリコントロールバーに追加されます。 デフォルトでは、メインコントロールバーは、デスクトップシステムおよび携帯電話のビューア領域の上部に表示され、タブレットのビューア領域の下部に移動します。 常に、使用可能なビューア全体の幅を使用します。 ビューアコンテナに対して、CSS内の色、高さ、垂直位置を変更できます。

メインコントロールバーの外観は、次のCSS クラスセレクターで制御されます。

`.s7ecatalogsearchviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p>ビューアの上部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p>ビューアの下部からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>メインコントロールバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 高さ36 ピクセルで、ビューアコンテナの上部に配置されたグレーのメインコントロールバーを設定します。

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

メインコントロールバーは、オプションのスクロール機能をサポートしています。 ビューアの幅が小さすぎて、コントロールバーのすべてのボタンのプリセットに合わせるのに十分なスペースがない場合にアクティブになります。 この場合、コントロールバーの右側に2状態矢印ボタンが表示されます。 このボタンをクリックまたはタップすると、スクロールボタンの状態に応じて、コントロールバーのすべての要素が左または右にスクロールされます。 この機能の主な使用例は、小さな画面を縦向きに配置したモバイルデバイスです。

スクロール機能はメインコントロールバーに対して有効になっており、セカンダリコントロールバーに対しては無効になっています。 この機能は、次のCSS クラスセレクターを使用してオンまたはオフになります。

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">位置</span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">静的</span>に設定すると、スクロール機能は無効になります。 </p> <p>スクロール機能を有効にするには、このプロパティを<span class="codeph">絶対</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

スクロールボタンは、ボタンを適切に配置する特殊なコンテナ要素に追加されます。 スクロールボタンの高さがコントロールバーの高さよりも小さい場合に備えて、ボタンの周りの領域とコントロールバーの背景の他の部分とは異なるスタイルを設定できます。

このスクロールボタンコンテナの外観は、次のCSS クラスセレクターで制御されます。

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>通常は、スクロールボタン自体の幅と同じか大きくする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>コンテナの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSSを使用して、スクロールボタン自体のサイズとスキンを調整できます。

このボタンの外観は、次のCSS クラスセレクターで制御されます。

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
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
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`および`selected`属性セレクターをサポートしています。これらのセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。 特に、`state="selected"`は、コントロールバーの内容を左にスクロールできる場合の最初のスクロールボタンの状態に対応します。 `state="default"`は、コンテンツが左側までスクロールされ、スクロールボタンが最初の状態に戻ることを提案する状態に対応します。

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

**例** – 携帯電話のメインコントロールバーでスクロール機能を有効にするには。 また、64 x 64 ピクセルのスクロールボタンを設定します。このボタンを選択した場合と選択しなかった場合は、4つのボタンの状態ごとに異なる画像が表示されます。

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


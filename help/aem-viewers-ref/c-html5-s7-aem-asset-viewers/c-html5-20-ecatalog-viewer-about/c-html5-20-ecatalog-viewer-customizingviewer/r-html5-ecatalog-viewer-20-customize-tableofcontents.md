---
title: 目次
description: 目次は、メインコントロールバーに配置されたボタンです。 アクティベートすると、ページインデックスとラベルのリストを含むドロップダウンパネルが表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 9b61e269-201d-4083-9c47-0b73d55aa6ed
TQID: 'https://experienceleague.adobe.com/DXw6lMxFxvi6DXB7-EI8kmZ3P-XpoWmaVt7NlHhQRRA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1116
ht-degree: 0%

---

# 目次{#table-of-contents}

目次は、メインコントロールバーに配置されたボタンです。 アクティベートすると、ページインデックスとラベルのリストを含むドロップダウンパネルが表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

設定に基づいて、リストには、カタログに存在するすべてのページを含めることも、明示的なラベルが定義されているページのみを含めることもできます。 デスクトップシステムでは、リストが使用可能な画面の不動産よりも長い場合、スクロールバーが右側に表示されます。

ビューアユーザーインターフェイスの目次ボタンの位置とサイズは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7tableofcontents
```

目次の&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーの上部からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> 行の最初のボタンの場合、左側の次のボタン、またはコントロールバーの左側までの距離。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> 目次ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p> 目次ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – メインコントロールバーの下部から4 ピクセル、左側から43 ピクセルに配置された目次ボタンを設定する。 サイズは28 x 28 ピクセルで、4つの異なるボタンの状態ごとに異なる画像が表示されます。

```
.s7ecatalogviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

ドロップダウンパネルの外観は、次のCSS クラスセレクターで制御されます。

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**ドロップダウンパネルのCSS プロパティ**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> ドロップダウンパネルの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p> パネル境界とコンテンツ間の内部オフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ボックス シャドウ </span> </p> </td> 
   <td colname="col2"> <p> パネルの周囲にドロップシャドウを配置します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>CSSからドロップダウンパネルのサイズや位置を制御することはできません。コンポーネントは、そのレイアウトをプログラムで管理します。

例 – 半透明の黒い背景、コンテンツの周囲に5 ピクセルの余白、およびドロップシャドウを持つドロップダウンパネルを設定します。

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

個々のアイテムのルックアンドフィールは、次のCSS クラスセレクターで制御されます。

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

項目の&#x200B;**CSS プロパティ**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>項目の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>内部パディング： </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>ドロップダウンリスト項目では、`state`属性セレクターをサポートしています。このセレクターを使用すると、様々なスキンを適用して、カーソルを合わせて選択した項目の状態を表示できます。

例 – Helvetica® 14 ピクセルのフォントと19 ピクセルの高さを持つドロップダウンアイテムを設定します。 選択した項目の上に濃いグレーの背景が表示され、薄いグレーの背景が表示されます。

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

ページインデックスを示す要素は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**ページインデックスのCSS プロパティ**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">分幅</span> </p> </td> 
   <td colname="col2"> <p> 最小要素の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p> エレメントの最大幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング右</span> </p> </td> 
   <td colname="col2"> <p> ページインデックスとページラベルの間の距離。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>`s7index` CSS クラスに`display:none`を設定すると、ページインデックスを完全に非表示にできます。

例1 – 最小幅が40 ピクセル、最大幅が70 ピクセル、右側に5 ピクセルのマージンを含むページインデックスを設定します。

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

例2 - ページインデックスを非表示：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

ページラベルは、次のCSS クラスセレクターで制御されます。

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

ページラベルの&#x200B;**CSS プロパティ**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">分幅</span> </p> </td> 
   <td colname="col2"> <p> 最小要素の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p> エレメントの最大幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 40 ピクセルの最小幅と240 ピクセルの最大幅でページインデックスを設定します。

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

ドロップダウンパネル内に垂直方向に収まる項目が多く、システムがデスクトップの場合、コンポーネントはパネルの右側に垂直スクロールバーをレンダリングします。 スクロールバー領域の外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

スクロールバーの&#x200B;**CSS プロパティ**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> スクロールバーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p> パネル領域の上部からオフセットされた垂直方向のスクロールバー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p> パネル領域の下部から垂直スクロールバーがオフセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p> パネル領域の右端から水平スクロールバーがオフセットされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 28 ピクセル幅のスクロールバーを設定し、パネルの上部、右側、または下部の領域に余白を設定します。

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

スクロールバートラックは、上と下のスクロールボタンの間の領域です。 コンポーネントは、トラックの位置と高さを自動的に設定します。 トラックは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

スクロール トラックの&#x200B;**CSS プロパティ**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>トラックの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>トラックの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 28 ピクセル幅で、半透明のグレーの背景を持つスクロールバートラックを設定します。

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

スクロールバーの親指は、スクロールトラック領域内で垂直方向に移動します。 垂直位置は、コンポーネントロジックによって制御されます。 ただし、コンテンツの量によっては、親指の高さが動的に変化することはありません。 次のCSS クラスセレクターを使用して、親指の高さやその他の要素を設定できます。

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

スクロールバーの親指の&#x200B;**CSS プロパティ**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>親指の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>親指の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディングトップ </span> </p> </td> 
   <td colname="col2"> <p> トラックの上部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング – 下</span> </p> </td> 
   <td colname="col2"> <p>トラックの下部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 特定のサムステートに対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumbは`state`属性セレクターをサポートしています。このセレクターを使用すると、`up`、`down`、`over`、および`disabled`の親指状態に異なるスキンを適用できます。

例 – 28 x 45 ピクセルのスクロールバーの親指を設定し、上下に10 ピクセルの余白があり、状態ごとに異なるアートワークを設定します。

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

上と下のスクロールボタンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

CSS `top`、`left`、`bottom`、`right`のプロパティを使用してスクロールボタンを配置することはできません。代わりに、ビューアーロジックによって自動的に配置されます。

上にスクロールして下にスクロールするボタンの&#x200B;**CSS プロパティ**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
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
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>ボタンは`state`属性セレクターをサポートしています。このセレクターを使用すると、`up`、`down`、`over`、`disabled`のボタン状態に異なるスキンを適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 28 x 32 ピクセルで、状態ごとに異なるアートワークを持つスクロールボタンを設定します。

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```

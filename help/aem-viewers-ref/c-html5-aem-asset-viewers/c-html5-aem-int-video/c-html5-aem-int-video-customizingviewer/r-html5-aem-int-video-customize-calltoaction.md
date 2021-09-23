---
title: 誘い文句（CTA、コールトゥアクション）
description: コールトゥアクションパネルは、ビデオが終了すると表示され、特定のビデオに関連付けられているすべてのインタラクティブスウォッチを表示します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 43e0ffb3-d650-4b79-ab48-2f32b313b832
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 2%

---

# 誘い文句（CTA、コールトゥアクション）{#call-to-action}

コールトゥアクションパネルは、ビデオが終了すると表示され、特定のビデオに関連付けられているすべてのインタラクティブスウォッチを表示します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

パネルは、ビデオタイトルを示すヘッダー領域、右上隅の再生ボタン、スクロール可能なグリッドとして表示される実際のインタラクティブスウォッチで構成されます。 設定属性[callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6)を使用して、パネルを無効にできます。

コールトゥアクションパネルは、常にビューア領域全体を使用します。

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

以下に示すCSSクラスセレクターで、コールトゥアクションパネルの背景色の外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction
```

## コールトゥアクションパネルの背景色のCSSプロパティ {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> コールトゥアクションパネルの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example}

背景色が濃いグレーのコールトゥアクションパネルを設定するには：

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

以下に示すCSSクラスセレクターで、コールトゥアクションパネルのヘッダーの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## コールトゥアクションパネルヘッダーのCSSプロパティ {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>ヘッダーの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ヘッダーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom  </span> </p> </td> 
   <td colname="col2"> <p>ヘッダーの下の境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-1}

高さ70ピクセルで、背景が濃いグレーで、下部にグレーの境界線がやや明るい2ピクセルのヘッダーを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

以下に示すCSSクラスセレクターで、コールトゥアクションパネルのヘッダータイトルの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## コールトゥアクションパネルのヘッダータイトルのCSSプロパティ：  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> バナー内のテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行の高さ  </span> </p> </td> 
   <td colname="col2"> <p>行の高さ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> フォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>バナー内のテキストの整列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left  </span> </p> </td> 
   <td colname="col2"> <p>左パディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right  </span> </p> </td> 
   <td colname="col2"> <p> 右パディング：「再生」ボタンのスペースを許可します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-2}

70ピクセルの線の高さ、25ピクセルのフォントサイズ、白の色および左揃えのビデオタイトルを設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

以下に示すCSSクラスセレクターで、コールトゥアクションパネルの閉じるボタンの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## コールトゥアクションパネルの閉じるボタンのCSSプロパティ： {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む、ヘッダーの上からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む、ヘッダーの右側からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>CSSスプライトを使用する場合は、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、 `state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

## 例 {#example-3}

28 x 28ピクセルの再生ボタンを設定するには、次のように記述します。 ボタンの位置は、ヘッダーの上端と右端から20ピクセルにする必要があります。 また、ボタンの4つの状態ごとに異なる画像を表示する必要があります。コンポーネントのスプライト画像からアートワークを取り出します。

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

以下に示すCSSクラスセレクターで、コールトゥアクションパネルのサムネールグリッドビューの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## コールトゥアクションパネルのサムネールグリッドビューのCSSプロパティ：  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>サムネール領域の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-4}

濃いグレーの背景を持つサムネール領域を設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

以下に示すCSSクラスセレクターで、コールトゥアクションパネルのサムセルの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## コールトゥアクションパネルのサムのセルのCSSプロパティ： {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周囲の水平および垂直のマージンのサイズ。 </p> <p>実際のサムネールの水平方向の間隔は、 <span class="codeph"> .s7thumbcell </span>に設定された左右のマージンの合計になります。 同じ規則が適用されますが、縦の間隔に適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-5}

24ピクセルの水平方向の間隔と18ピクセルの垂直方向の間隔を設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

以下に示すCSSクラスセレクターで、コールトゥアクションパネルのサムネールの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## コールトゥアクションパネルのサムネールのCSSプロパティ： {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>サムネールの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムネールでは、 `state`属性セレクターがサポートされます。このセレクターは、サムネールの状態ごとに異なるスキンを適用するのに使用できます。 特に、`state="selected"`は現在選択されている画像のサムネールに対応します。`state="default"`は、残りのサムネールに対応します。`state="over"`は、マウスカーソルを合わせたときに使用されます。

## 例 {#example-6}

94 x 100ピクセルのサムネールを設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

以下に示すCSSクラスセレクターで、コールトゥアクションパネルのサムネールラベルの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## コールトゥアクションパネルのサムネールラベルのCSSプロパティ： {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> ラベルのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>ラベルの水平方向の整列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>フォント名 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-7}

白の色を使用するラベルを設定するには、中央揃えで15ピクセル、Arial®フォントを使用します。

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

垂直方向に表示できる数より多いサムネールがある場合、サムネールは右側に垂直方向のスクロールバーをレンダリングします。 デフォルトでは、コールトゥアクションパネルは、サムやスクロールボタンのない小さな縦棒をレンダリングします。 ただし、ビューアのCSSを変更してバーをカスタマイズすることはできます。

以下に示すCSSクラスセレクターで、コールトゥアクションパネルのスクロールバー領域の外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## コールトゥアクションパネルのスクロールバー領域のCSSプロパティ： {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> スクロールバーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>サムネール領域の上部からのスクロールバーの垂直方向のオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>サムネール領域の下端からのスクロールバーの垂直方向のオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> サムネール領域の右端からのスクロールバーの水平方向のオフセット。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-8}

幅が22ピクセルで、サムネール領域の上、右または下からの余白がないスクロールバーを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

スクロールバートラックは、上下のスクロールバーボタンの間の領域です。 このコンポーネントは、トラックの位置と高さを自動的に設定します。

以下に示すCSSクラスセレクターで、コールトゥアクションパネルのスクロールバートラックの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## スクロールトラックバーのCSSプロパティ {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>スクロールトラックバーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>トラックバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-9}

幅が22ピクセルで、グレー色のスクロールバートラックを設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

スクロールバーサムは、スクロールトラック領域内で垂直方向に移動します。 垂直方向の位置は、コンポーネントのロジックで完全に制御されます。ただし、サムの高さはコンテンツの量に応じて動的に変化するわけではありません。

次のCSSクラスセレクターで、サムの高さの外観とその他の要素を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## コールトゥアクションパネルのサムの高さのCSSプロパティ： {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>サムの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>サムの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top  </span> </p> </td> 
   <td colname="col2"> <p>トラックの上部間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom  </span> </p> </td> 
   <td colname="col2"> <p>トラックの下端との間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>サムのカラー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> サムの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムでは、 `state`属性セレクターがサポートされます。このセレクターは、次のサムの状態ごとに異なるスキンを適用するのに使用できます。`"up"`、`"down"`、`"over"`、および`"disabled"`です。

## 例 {#example-10}

6 x 167ピクセルで、3ピクセルの丸い角とグレーの色を持つスクロールバーサムを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

以下に示すCSSクラスセレクターで、上下のスクロールボタンの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

CSSのtop、left、bottomまたはrightプロパティを使用してスクロールボタンを配置することはできません。ビューアのロジックによって、自動的に配置が決まります。 インタラクティブビデオビューアのコールトゥアクションパネルでは、スクロールバーのこれらのボタンは使用されないので、初期設定のCSSではサイズが0ピクセルに設定されています。

## コールトゥアクションパネルの上下のスクロールボタンのCSSプロパティ：  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>これらのボタンでは、 `state`属性セレクターがサポートされます。このセレクターは、次のサムの状態ごとに異なるスキンを適用するのに使用できます。`"up"`、`"down"`、`"over"`、および`"disabled"`です。

ボタンのツールチップはローカライズできます。 [ユーザインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

## 例 {#example-11}

スクロールボタンのサイズを0に設定して非表示にすることで、スクロールボタンを無効にします。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```

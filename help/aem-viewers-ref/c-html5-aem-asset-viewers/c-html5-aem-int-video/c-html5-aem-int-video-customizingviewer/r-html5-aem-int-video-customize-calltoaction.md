---
title: 誘い文句（CTA、コールトゥアクション）
description: call to actionパネルは、ビデオが終了すると表示され、特定のビデオに関連付けられているすべてのインタラクティブスウォッチが表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 43e0ffb3-d650-4b79-ab48-2f32b313b832
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 1%

---

# 誘い文句（CTA、コールトゥアクション）{#call-to-action}

call to actionパネルは、ビデオが終了すると表示され、特定のビデオに関連付けられているすべてのインタラクティブスウォッチが表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

このパネルは、ビデオのタイトルを示すヘッダー領域、右上隅の再生ボタン、スクロール可能なグリッドとして表示される実際のインタラクティブスウォッチで構成されます。 [callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6) 設定属性を使用して、パネルを無効にできます。

call to action パネルには、常に使用可能なビューア領域全体が表示されます。

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

次の CSS クラスセレクターは、call to action パネルでの背景色の外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction
```

## call to actionパネルの背景色の CSS プロパティ {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> call to actionパネルの背景色 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example}

背景がダークグレーのcall to action パネルを設定するには：

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

次の CSS クラスセレクターは、call to action パネルでのヘッダーの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## call to action パネルヘッダーの CSS プロパティ {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>ヘッダーの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ヘッダーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom </span> </p> </td> 
   <td colname="col2"> <p>ヘッダーの下のボーダー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-1}

高さが 70 ピクセルで、背景が濃いグレー、下部に沿って 2 ピクセルの境界線がわずかに明るいグレーのヘッダーを設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

次の CSS クラスセレクターは、call to action パネルでのヘッダータイトルの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## call to actionパネルのヘッダータイトルの CSS プロパティ：  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> バナー内のテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>行の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p> フォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>バナー内のテキストの配置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left </span> </p> </td> 
   <td colname="col2"> <p>左パディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right </span> </p> </td> 
   <td colname="col2"> <p> 再生ボタンのスペースを確保するための右パディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-2}

高さ 70 ピクセル、フォントサイズ 25 ピクセル、白色および左揃えを使用してビデオタイトルを設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

次の CSS クラスセレクターは、call to actionパネルでの「閉じる」ボタンの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## call to actionパネルの「閉じる」ボタンの CSS プロパティ： {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>ヘッダーの上からパディングを含めて配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>ヘッダーの右からパディングを含めて配置します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p> ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>CSS スプライトを使用する場合は、アートワークスプライトの内側に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態に応じて異なるスキンを適用するために使用できる `state` 属性セレクターをサポートしています。

## 例 {#example-3}

28 x 28 ピクセルの再生ボタンを設定します。 ボタンは、ヘッダーの上と右端から 20 ピクセルの位置に配置する必要があります。 また、4 つの異なるボタンの状態ごとに異なる画像を表示する必要があります。は、コンポーネントのスプライト画像からアートワークを取得します。

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

次の CSS クラスセレクターは、call to action パネルのサムネールグリッドビューの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## call to actionパネルのサムネールグリッドビューの CSS プロパティ：  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>サムネール領域の背景色 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-4}

濃いグレーの背景でサムネール領域を設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

次の CSS クラスセレクターは、call to action パネルのサムセルの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## call to action パネルのサムセルの CSS プロパティ： {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周囲の水平および垂直の余白のサイズ。 </p> <p>実際の水平方向のサムネールの間隔は、.s7thumbcell <span class="codeph"> に設定された左右の余白 </span> 合計と等しくなります。 同じルールが、垂直方向の間隔にも適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-5}

水平方向の間隔を 24 ピクセル、垂直方向の間隔を 18 ピクセルに設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

次の CSS クラスセレクターは、call to action パネルでのサムネールの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## call to actionパネルのサムネールの CSS プロパティ： {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>サムネールのボーダー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムネールでは `state` 属性セレクターがサポートされており、これを使用して異なるスキンを異なるサムネール状態に適用できます。 特に、`state="selected"` は、現在選択されている画像のサムネールに対応します。`state="default"` は、残りのサムネールに対応します。`state="over"` は、マウスのカーソルを合わせたときに使用されます。

## 例 {#example-6}

94 x 100 ピクセルのサムネールを設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

次の CSS クラスセレクターは、call to action パネルでのサムネールラベルの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## call to actionパネルのサムネールラベルの CSS プロパティ： {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> ラベルのテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>ラベルの水平方向揃え。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-7}

白を使用するラベルを設定するには、中央に 15 ピクセル配置し、Arial® フォントを使用します。

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

縦に表示しきれない数のサムネールがある場合、サムネールは右側に縦のスクロールバーをレンダリングします。 デフォルトでは、call to action パネルは、サムボタンとスクロールボタンのない小さな垂直バーをレンダリングします。 ただし、ビューアの CSS を変更することで、バーをカスタマイズすることができます。

次の CSS クラスセレクターは、call to action パネルのスクロールバー領域の外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## call to action パネルのスクロールバー領域の CSS プロパティ： {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> スクロールバーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>サムネール領域の上部からの垂直スクロールバーのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>サムネール領域の下部からの垂直スクロールバーのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> サムネール領域の右端からの水平スクロールバーのオフセット。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-8}

幅 22 ピクセルで、サムネール領域の上、右または下から余白を持たないスクロールバーを設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

スクロールバートラックは、上部と下部のスクロールバーボタンの間の領域です。 トラックの位置と高さが自動的に設定されます。

次の CSS クラスセレクターは、call to action パネルでのスクロールバートラックの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## スクロールトラックバーの CSS プロパティ {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>スクロール トラック バーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>トラックバーの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-9}

幅 22 ピクセルで灰色のスクロールバーのトラックを設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

スクロールバーの親指は、スクロールトラック領域内で垂直に移動します。 垂直方向の位置はコンポーネントロジックによって完全に制御されますが、コンテンツの量に応じて親指の高さが動的に変化することはありません。

次の CSS クラスセレクターは、親指の高さなどのアスペクトの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## call to action パネルのサムハイトの CSS プロパティ： {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>親指の幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>親指高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>トラックの上部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p>トラックの下部の間の垂直方向のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>親指のカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 特定のサムネール状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb では、`state` 属性セレクターをサポートしています。このセレクターを使用して、`"up"`、`"down"`、`"over"` および `"disabled"` の異なるサムステートに異なるスキンを適用できます。

## 例 {#example-10}

6 x 167 ピクセルのスクロールバーの親指を設定するには、3 つの丸いコーナーとグレーのカラーを使用します。

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

次の CSS クラスセレクターは、上部と下部のスクロールボタンの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

CSS の top、left、bottom または right プロパティを使用してスクロールボタンを配置することはできません。スクロールボタンはビューロジックにより自動的に配置されます。 インタラクティブビデオビューアのcall to action パネルでは、これらのボタンはスクロールバーで使用しないので、デフォルトの CSS ではサイズは 0 ピクセルに設定されます。

## call to action パネルの上下のスクロールボタンの CSS プロパティ：  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> ボタンの幅。 </p> </td> 
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
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>これらのボタンは、`state` 属性セレクターをサポートしています。このセレクターを使用して、`"up"`、`"down"`、`"over"` および `"disabled"` の異なる親指状態に異なるスキンを適用できます。

ボタンのツールチップはローカライズできます。 [ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

## 例 {#example-11}

スクロールボタンのサイズを 0 に設定して非表示にすることにより、スクロールボタンを無効にします。

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

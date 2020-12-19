---
description: 誘い文句（CTA：コールトゥアクション）パネルは、ビデオが終了すると表示され、特定のビデオに関連付けられたすべてのインタラクティブスウォッチが表示されます。
seo-description: 誘い文句（CTA：コールトゥアクション）パネルは、ビデオが終了すると表示され、特定のビデオに関連付けられたすべてのインタラクティブスウォッチが表示されます。
seo-title: 誘い文句（CTA、コールトゥアクション）
solution: Experience Manager
title: 誘い文句（CTA、コールトゥアクション）
topic: Dynamic media
uuid: 04a042d8-7329-4f1d-b3b9-312d620b1f29
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1298'
ht-degree: 3%

---


# 誘い文句（CTA、コールトゥアクション）{#call-to-action}

誘い文句（CTA：コールトゥアクション）パネルは、ビデオが終了すると表示され、特定のビデオに関連付けられたすべてのインタラクティブスウォッチが表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

パネルは、ビデオタイトルを示すヘッダー領域、右上隅の再生ボタンおよびスクロール可能なグリッドとして表示される実際のインタラクティブスウォッチで構成されます。 [callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6)設定属性を使用して、パネルを無効にできます。

誘い文句（CTA：コールトゥアクション）パネルは、常にビューアの使用可能な領域全体を占めます。

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

以下に示すCSSクラスセレクターで、誘い文句（CTA：コールトゥアクション）パネルの背景色の外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction
```

## 誘い文句（CTA：コールトゥアクションパネル）{#css-properties-of-the-background-color-of-the-call-to-action-panel}の背景色のCSSプロパティ

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 誘い文句（CTA：コールトゥアクション）パネルの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example}

ダークグレーの背景色の誘い文句（CTA：コールトゥアクション）パネルを設定するには：

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

以下に示すCSSクラスセレクターで、「アクションの呼び出し」パネルのヘッダーの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## 誘い文句（CTA：コールトゥアクション）パネルヘッダー{#css-properties-of-the-call-to-action-panel-header}のCSSプロパティ

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

高さが70ピクセルで、背景色が濃いグレーで、下端にわずかに明るい灰色の2ピクセルの境界線があるヘッダーを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

以下に示すCSSクラスセレクターで、誘い文句（CTA：コールトゥアクション）パネルのヘッダータイトルの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## 誘い文句（CTA：コールトゥアクション）パネルのヘッダータイトルのCSSプロパティ： {#css-properties-of-the-header-title-in-the-call-to-action-panel}

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
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p>行の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> フォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>バナー内のテキストの配置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left  </span> </p> </td> 
   <td colname="col2"> <p>左パディング </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right  </span> </p> </td> 
   <td colname="col2"> <p> 右パディング。「再生」ボタンのスペースを許可します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-2}

行の高さが70ピクセル、フォントサイズが25ピクセル、白、左揃えのビデオタイトルを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

以下に示すCSSクラスセレクターで、呼び出し先アクションパネルの閉じるボタンの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## 誘い文句（CTA：コールトゥアクション）パネルの閉じるボタンのCSSプロパティ：{#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む、ヘッダーの上端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む、ヘッダーの右からの位置。 </p> </td> 
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
   <td colname="col2"> <p>ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

## 例 {#example-3}

28 x 28ピクセルの再生ボタンを設定するには、次のように記述します。ヘッダーの上端から右端まで20ピクセルの位置に配置します。ボタンの4つの状態ごとに異なる画像を表示します。コンポーネントのスプライト画像からアートワークを取得します。

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

以下に示すCSSクラスセレクターで、呼び出し元アクションパネルでのサムネールグリッド表示の外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## 誘い文句（CTA：コールトゥアクション）パネルのサムネールグリッド表示のCSSプロパティ： {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>サムネール領域の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-4}

暗いグレーの背景のサムネール領域を設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

以下に示すCSSクラスセレクターで、「アクションの呼び出し」パネルのサムのセルの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## 誘い文句（CTA：コールトゥアクション）パネルのサムネールのCSSプロパティ{#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネール周囲の水平方向および垂直方向のマージンのサイズ。 </p> <p>実際のサムネールの水平方向の間隔は、<span class="codeph"> .s7thumbcell </span>に設定された左右のマージンの合計になります。 同じ規則が適用されますが、垂直方向の間隔には適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#example-5}

24ピクセルの水平方向の間隔と18ピクセルの垂直方向の間隔を設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

以下に示すCSSクラスセレクターで、「呼び出し先アクション」パネルでのサムネールの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## 誘い文句（CTA：コールトゥアクション）パネルのサムネールのCSSプロパティ{#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

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
>サムネールでは、`state`属性セレクターがサポートされます。このセレクターは、サムネールの状態ごとに異なるスキンを適用するのに使用できます。 具体的には、`state="selected"`は現在選択されている画像のサムネールに対応します。`state="default"`は、その他のサムネールに対応します。`state="over"`は、マウスカーソルを合わせたときに使用されます。

## 例 {#example-6}

94 x 100ピクセルのサムネールを設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

以下に示すCSSクラスセレクターで、呼び出しアクションパネルでのサムネールラベルの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## 誘い文句（CTA：コールトゥアクション）パネルのサムネールラベルのCSSプロパティ{#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> ラベルのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>ラベルの水平方向の位置。 </p> </td> 
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

白の色を使用するラベルを設定するには、中央揃えで15ピクセル、Arialフォントを使用します。

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

垂直方向に表示に収まらないサムネールがある場合は、サムネールの右側に垂直方向のスクロールバーが表示されます。 デフォルトでは、誘い文句（CTA：コールトゥアクション）パネルには、サムボタンとスクロールボタンのない小さな縦棒がレンダリングされます。 ただし、ビューアのCSSを変更してバーをカスタマイズすることはできます。

以下に示すCSSクラスセレクターで、「アクションを呼び出し」パネルのスクロールバー領域の外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## 誘い文句（CTA：コールトゥアクション）パネルのスクロールバー領域のCSSプロパティ。{#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> スクロールバーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>サムネール領域の上端からのスクロールバーの垂直方向のオフセット。 </p> </td> 
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

幅が22ピクセルで、サムネール領域の上、右または下からのマージンがないスクロールバーを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

スクロールバートラックは、スクロールバーの上部ボタンと下部ボタンの間の領域です。 トラックの位置と高さが自動的に設定されます。

以下に示すCSSクラスセレクターで、「アクションを呼び出し」パネルのスクロールバートラックの外観を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## スクロールトラックバー{#css-properties-of-the-scroll-track-bar}のCSSプロパティ

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

幅が22ピクセルで、グレーのスクロールバートラックを設定するには：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

スクロールバーサムは、スクロールトラック領域内で垂直方向に移動します。 その垂直方向の位置は、コンポーネントのロジックによって完全に制御されます。ただし、サムの高さは、コンテンツの量に応じて動的に変化するわけではありません。

以下に示すCSSクラスセレクターで、サムの高さの外観とその他の縦横比を制御します。

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## 誘い文句（CTA：コールトゥアクション）パネルのサムの高さのCSSプロパティ{#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

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
   <td colname="col2"> <p>トラックの上端との間の垂直方向のパディング。 </p> </td> 
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
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムでは、`state`属性セレクターがサポートされます。このセレクターは、サムの次の状態ごとに異なるスキンを適用するのに使用できます。`"up"`、`"down"`、`"over"`、および`"disabled"`。

## 例 {#example-10}

6 x 167ピクセルで、角が3ピクセル、グレーのスクロールバーサムを設定するには、次のように記述します。

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

CSSのtop、left、bottomまたはrightプロパティを使用してスクロールボタンを配置することはできません。ビューアのロジックによって自動的に配置が決まります。 インタラクティブビデオビューアの誘い文句(CSS)パネルでは、スクロールバーのこれらのボタンは使用されないので、初期設定のCSSではサイズが0ピクセルに設定されています。

## 誘い文句（CTA：コールトゥアクション）パネルの上下のスクロールボタンのCSSプロパティ。 {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

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
   <td colname="col2"> <p>ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>これらのボタンでは、`state`属性セレクターがサポートされます。このセレクターは、サムの次の状態ごとに異なるスキンを適用するのに使用できます。`"up"`、`"down"`、`"over"`、および`"disabled"`。

ボタンのツールヒントをローカライズできます。 [ユーザインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

## 例 {#example-11}

スクロールボタンのサイズを0に設定し、非表示にして、スクロールボタンを無効にします。

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


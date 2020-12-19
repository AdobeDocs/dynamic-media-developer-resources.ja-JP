---
description: インタラクティブデータが設定でビューアに渡されると、インタラクティブスウォッチパネルがビデオコンテンツの横に表示されます。 上部に表示されるバナーは、「クリックして表示」、1つ以上のインタラクティブスウォッチの列、2つのスクロールボタン（デスクトップシステムのみ）などのテキストをレンダリングします。
seo-description: インタラクティブデータが設定でビューアに渡されると、インタラクティブスウォッチパネルがビデオコンテンツの横に表示されます。 上部に表示されるバナーは、「クリックして表示」、1つ以上のインタラクティブスウォッチの列、2つのスクロールボタン（デスクトップシステムのみ）などのテキストをレンダリングします。
seo-title: インタラクティブスウォッチ
solution: Experience Manager
title: インタラクティブスウォッチ
topic: Dynamic media
uuid: 9f9df764-3dd0-414e-a0db-4287f0019313
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 2%

---


# インタラクティブスウォッチ{#interactive-swatches}

インタラクティブデータが設定でビューアに渡されると、インタラクティブスウォッチパネルがビデオコンテンツの横に表示されます。 上部に表示されるバナーは、「クリックして表示」、1つ以上のインタラクティブスウォッチの列、2つのスクロールボタン（デスクトップシステムのみ）などのテキストをレンダリングします。

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

デスクトップシステムおよびタッチデバイスでは、横置きレイアウトでは、インタラクティブスウォッチがビデオコンテンツの右に縦にレンダリングされます。 縦置きのタッチデバイスでは、スウォッチはビューアの下部に水平方向の行として表示されます。

以下に示すCSSクラスセレクターで、インタラクティブスウォッチパネルの位置と方向を制御します。

```
.s7interactivevideoviewer .s7interactiveswatches
```

## インタラクティブスウォッチのCSSプロパティ{#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの上部の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの下の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの左側の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの右側の位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

インタラクティブスウォッチパネルの実行時の場所と向きは、上記のCSSプロパティを次のように組み合わせて定義します。

* インタラクティブスウォッチをビューアの下部で水平方向にレンダリングするには、高さを絶対ピクセル値に設定します。left, bottom to 0px;width, right, top to auto
* インタラクティブスウォッチをビデオコンテンツの右側に垂直方向にレンダリングするには、幅を絶対ピクセルに設定します。rightとtop to 0px;height, left, bottom to auto

このスタイル設定とCSSマーカーを組み合わせて使用すると、インタラクティブスウォッチパネルを適切に配置できます。

## 例 {#example}

タッチデバイスで横置きの方向にビューアの下部に水平方向にレンダリングし、その他の場合はビデオコンテンツの右に垂直方向に表示するインタラクティブスウォッチパネルを設定するには、次のように記述します。

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

バナーのサイズと位置は、インタラクティブスウォッチコンポーネントによって、CSSで適用された他のスタイル設定に基づいて管理され、明示的に設定することはできません。

以下に示すCSSクラスセレクターで、バナーパネルの外観を制御します。

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## バナーパネルのCSSプロパティ{#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>バナーパネルの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-重み付け  </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォント重み付け。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントサイズです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントの整列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

バナーのツールチップをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

背景色が濃いグレー、2ピクセルの境界線が明るいグレー、水平方向に中央揃えされた白のテキストのバナーを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

以下に示すCSSクラスセレクターで、スウォッチの外観を制御します。

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## スウォッチ領域のCSSプロパティ{#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>スウォッチ領域の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-9cadd62a09fd44a280f55ff42437e416}

背景色が濃いグレーのスウォッチ領域を設定するには、次の手順に従います。

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

以下に示すCSSクラスセレクターで、スウォッチサムネールの間隔を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## スウォッチのサムネールの間隔{#css-properties-of-the-swatches-thumbnail-spacing}のCSSプロパティ

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネール周囲の水平方向および垂直方向のマージンのサイズ。 実際のサムネールの間隔は、<span class="codeph"> .s7thumbcell </span>に設定された左右のマージンの合計になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-39fb270b7e494a9d99e6e8f6890ec53c}

10ピクセルにする垂直方向の間隔を設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

以下に示すCSSクラスセレクターで、個々のサムネールの外観を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## 個々のサムネールの外観のCSSプロパティ{#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
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
>サムネールでは、`state`属性セレクターがサポートされます。このセレクターは、サムネールの状態ごとに異なるスキンを適用するのに使用できます。 特に、`state="selected"`は、現在選択されている画像のサムネールに対応します。`state="default"`は、その他のサムネールに対応します。`state="over"`は、マウスカーソルを合わせたときに使用されます。

## 例 {#section-69fec189ffaa440b97b6b846c320b75b}

100 x 75ピクセルのサムネールを設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

以下に示すCSSクラスセレクターで、サムネールラベルの外観を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## サムネールラベル{#css-properties-of-the-appearance-of-the-thumbnail-label}の外観のCSSプロパティ

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>テキストカラー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>ラベルの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>テキストの水平方向揃え。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>フォント名 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-eb141eb6c1154183baa69796edb90536}

左揃え、白、12ピクセル、Helveticaフォント、下の境界線を使用するラベルを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

以下に示すCSSクラスセレクターで、上下のスクロールボタンの外観を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

CSS `top`、`left`、`bottom`、`right`の各プロパティを使用してスクロールボタンを配置することはできません。ビューアのロジックによって自動的に配置が決まります。

## 上下のスクロールボタン{#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}の外観のCSSプロパティ

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>ボタンの特定の状態に対して表示する画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state`属性セレクターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。&quot; `up`&quot;、&quot; `down`&quot;、&quot; `over`&quot;、&quot; `disabled`&quot;

ボタンのツールヒントをローカライズできます。 詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

## 例 {#section-e6ce4fa084b84288bc7583342b2c510c}

60 x 36ピクセルで、状態ごとに異なるアートワークを持ち、コンポーネントのスプライト画像からそのアートワークを取得するスクロールアップボタンを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```


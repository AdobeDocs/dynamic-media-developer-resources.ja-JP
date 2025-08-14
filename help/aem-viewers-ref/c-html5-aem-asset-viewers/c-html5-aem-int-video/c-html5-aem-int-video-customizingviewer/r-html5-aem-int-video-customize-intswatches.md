---
title: インタラクティブスウォッチ
description: 設定でインタラクティブデータがビューアに渡されると、ビデオコンテンツの横にインタラクティブスウォッチパネルが表示されます。 これは、「クリックして表示」などのテキストをレンダリングする上部のバナー、1 つ以上のインタラクティブスウォッチの列、2 つのスクロールボタン（デスクトップシステムでのみ使用可能）で構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# インタラクティブスウォッチ{#interactive-swatches}

設定でインタラクティブデータがビューアに渡されると、ビデオコンテンツの横にインタラクティブスウォッチパネルが表示されます。 これは、「クリックして表示」などのテキストをレンダリングする上部のバナー、1 つ以上のインタラクティブスウォッチの列、2 つのスクロールボタン（デスクトップシステムでのみ使用可能）で構成されます。

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

デスクトップシステムとタッチデバイスでは、横向きでは、インタラクティブスウォッチがビデオコンテンツの右側に垂直にレンダリングされます。 縦向きのタッチデバイスでは、ビューアの下部に水平方向のスウォッチとして表示されます。

次の CSS クラスセレクターは、インタラクティブスウォッチパネルの場所と方向を制御します。

```
.s7interactivevideoviewer .s7interactiveswatches
```

## インタラクティブスウォッチの CSS プロパティ {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの上部。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの下位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの左側の位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの右位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

インタラクティブスウォッチパネルの実行時の場所と向きは、次のように上記の CSS プロパティの組み合わせによって定義されます。

* ビューアの下部でインタラクティブスウォッチを水平方向にレンダリングするには、高さを絶対ピクセル値に、左と下を 0px に、幅、右と上を自動に設定します。
* インタラクティブスウォッチをビデオコンテンツの右側に垂直方向にレンダリングするには、幅を絶対ピクセルに、右上を 0px に、高さ、左および下を自動に設定します。

このスタイル設定で CSS マーカーを使用して、インタラクティブスウォッチパネルをアダプティブに配置できます。

## 例 {#example}

タッチデバイスのビューアの下部で水平方向にレンダリングされるようにインタラクティブスウォッチパネルを横向きに設定します。 それ以外の場合は、ビデオコンテンツの右側に垂直方向に表示する場合は、次のようにします。

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

バナーのサイズと位置は、CSS で適用された他のスタイル設定に基づいてインタラクティブスウォッチコンポーネントによって管理され、明示的に設定することはできません。

次の CSS クラスセレクターで、バナーパネルの外観を制御します。

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## バナーパネルの CSS プロパティ {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>バナーパネルの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>バナーパネルの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントサイズです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントの配置を指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

バナーツールチップはローカライズ可能である。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

濃いグレーの背景、明るいグレーの 2 ピクセルの境界線、水平方向に中央に置かれた白いテキストのバナーを設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

次の CSS クラスセレクターで、スウォッチの外観を制御します。

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## スウォッチ領域の CSS プロパティ {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>スウォッチ領域の背景色 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-9cadd62a09fd44a280f55ff42437e416}

背景がダークグレーのスウォッチ領域を設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

次の CSS クラスセレクターで、スウォッチのサムネール間の間隔を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## スウォッチのサムネール間隔の CSS プロパティ {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周囲の水平方向と垂直方向の余白のサイズ。 実際のサムネールの間隔は、.s7thumbcell <span class="codeph"> に設定された左右の余白 </span> 合計と等しくなります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-39fb270b7e494a9d99e6e8f6890ec53c}

垂直方向の間隔を 10 ピクセルに設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

次の CSS クラスセレクターは、個々のサムネールの外観を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## 個々のサムネールのアピアランスに関する CSS プロパティ {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
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
>サムネールでは `state` 属性セレクターがサポートされており、これを使用して異なるスキンを異なるサムネール状態に適用できます。 特に、`state="selected"` は、現在選択されている画像のサムネールに対応します。`state="default"` は、残りのサムネールに対応します。`state="over"` は、マウスをポイントしたときに使用されます。

## 例 {#section-69fec189ffaa440b97b6b846c320b75b}

100 x 75 ピクセルのサムネールを設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

次の CSS クラスセレクターで、サムネールラベルの外観を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## サムネールラベルのアピアランスに関する CSS プロパティ {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>テキストのカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>ラベルの境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>テキストの水平方向の配置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-eb141eb6c1154183baa69796edb90536}

左揃えの白 12 ピクセルを使用するラベルを Helvetica® フォントおよび下罫線で設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

次の CSS クラスセレクターで、上下のスクロールボタンの外観を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

CSS `top`、`left`、`bottom` および `right` プロパティを使用してスクロールボタンを配置することはできません。代わりに、ビューアロジックによって自動的に配置されます。

## 上下のスクロールボタンの外観に関する CSS プロパティ {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>スクロール ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>CSS スプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p>CSS スプライト <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ール </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、ボタンの状態（「`state`」、「`up`」、「`down`」、「`over`」）に異なるスキンを適用するために使用できる `disabled` 属性セレクターがサポートされています。

ボタンのツールチップはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

## 例 {#section-e6ce4fa084b84288bc7583342b2c510c}

スクロールアップボタンを 60 x 36 ピクセルに設定するには、状態ごとに異なるアートワークを使用し、そのアートワークをコンポーネントのスプライト画像から取得します。

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

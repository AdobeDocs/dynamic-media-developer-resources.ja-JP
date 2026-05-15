---
title: インタラクティブスウォッチ
description: インタラクティブデータが設定でビューアに渡された場合、インタラクティブスウォッチ パネルがビデオコンテンツの横に表示されます。 上部のバナーで構成され、「クリックして表示」などのテキストがレンダリングされます。また、1つ以上のインタラクティブなスウォッチの列と2つのスクロールボタンが表示されます（デスクトップシステムでのみ使用できます）。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
TQID: 'https://experienceleague.adobe.com/40q8-9AJ1jcuAURbTj3HGo-dihtEX-UOzkwcWf0UapY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 900
ht-degree: 0%

---

# インタラクティブスウォッチ{#interactive-swatches}

インタラクティブデータが設定でビューアに渡された場合、インタラクティブスウォッチ パネルがビデオコンテンツの横に表示されます。 上部のバナーで構成され、「クリックして表示」などのテキストがレンダリングされます。また、1つ以上のインタラクティブなスウォッチの列と2つのスクロールボタンが表示されます（デスクトップシステムでのみ使用できます）。

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

デスクトップシステムやタッチデバイスでは、横向きのインタラクティブなスウォッチがビデオコンテンツの右側に垂直方向にレンダリングされます。 ポートレート方向のタッチデバイスでは、これらは水平方向のスウォッチとして、ビューアの下部に表示されます。

次のCSS クラスセレクターは、インタラクティブスウォッチパネルの位置と方向を制御します。

```
.s7interactivevideoviewer .s7interactiveswatches
```

## インタラクティブスウォッチのCSS プロパティ {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの上部位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの下部位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">さんが</span>を残しました </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの左端。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>インタラクティブスウォッチパネルの右位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

インタラクティブなスウォッチパネルの実行時の場所と方向は、上記のCSS プロパティの組み合わせで次のように定義されます。

* インタラクティブなスウォッチをビューアの下部で水平方向にレンダリングするには、高さを絶対ピクセル値に設定し、左と下を0px、幅、右、上を自動に設定します。
* インタラクティブスウォッチをビデオコンテンツの右側に垂直方向にレンダリングするには、幅を絶対ピクセルに設定します。右と上を0 pxに、高さ、左と下を自動に設定します。

このスタイル設定でCSS マーカーを使用すると、インタラクティブなスウォッチパネルのアダプティブな配置を実現できます。

## 例 {#example}

インタラクティブなスウォッチパネルを設定して、横方向のタッチデバイスでビューアの下部に水平方向にレンダリングする。 その他のすべての場合に、ビデオコンテンツの右側に垂直方向に表示するには：

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

バナーのサイズと位置は、CSSで適用される他のスタイルに基づいてインタラクティブ スウォッチ コンポーネントによって管理され、明示的に設定することはできません。

次のCSS クラスセレクターは、バナーパネルの外観を制御します。

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## バナーパネルのCSS プロパティ {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>バナーパネルの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>バナーパネルの周囲の境界線。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>バナーパネル内のテキストに使用するフォントの整列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

バナーツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

暗いグレーの背景を持つバナーを設定するには、明るいグレーの2 ピクセルの境界線と白いテキストを水平方向に中央に配置します。

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

次のCSS クラスセレクターは、スウォッチの外観を制御します。

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## スウォッチ領域のCSS プロパティ {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>スウォッチ領域の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-9cadd62a09fd44a280f55ff42437e416}

暗いグレーの背景でスウォッチ領域を設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

次のCSS クラスセレクターは、スウォッチサムネールの間隔を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## スウォッチのサムネール間隔のCSS プロパティ {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周りの水平および垂直余白のサイズ。 実際のサムネールの間隔は、<span class="codeph"> .s7thumbcell </span>に設定された左右の余白の合計と等しくなります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-39fb270b7e494a9d99e6e8f6890ec53c}

垂直方向の間隔を10 ピクセルに設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

次のCSS クラスセレクターは、個々のサムネールの外観を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## 個々のサムネールの外観のCSS プロパティ {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>サムネールの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムネールは`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるサムネール状態に異なるスキンを適用できます。 特に、`state="selected"`は現在選択されている画像のサムネールに対応し、`state="default"`は残りのサムネールに対応し、`state="over"`はマウスオーバーで使用されます。

## 例 {#section-69fec189ffaa440b97b6b846c320b75b}

100 x 75 ピクセルのサムネールを設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

次のCSS クラスセレクターは、サムネールラベルの外観を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## サムネールラベルのアピアランスのCSS プロパティ {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>テキストの色： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>ラベルの境界線： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> テキスト整列</span> </p> </td> 
   <td colname="col2"> <p>横組みテキストの整列： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-eb141eb6c1154183baa69796edb90536}

左揃え、白、12 ピクセル、Helvetica® フォント、および下部の境界線を使用するようにラベルを設定するには：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

次のCSS クラスセレクターは、上下スクロールボタンの外観を制御します。

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

CSS `top`、`left`、`bottom`、`right`のプロパティを使用してスクロールボタンを配置することはできません。代わりに、ビューアーロジックによって自動的に配置されます。

## 上下スクロールボタンのアピアランスのCSS プロパティ {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>スクロールボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>CSS スプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、ボタンの状態（「`up`」、「`down`」、「`over`」、「`disabled`」など）に異なるスキンを適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

## 例 {#section-e6ce4fa084b84288bc7583342b2c510c}

60 x 36 ピクセルのスクロールアップボタンを設定するには、ステートごとに異なるアートワークを持ち、そのアートワークをコンポーネントのスプライト画像から取り込みます。

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

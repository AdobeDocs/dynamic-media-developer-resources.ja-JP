---
description: ビデオスクラバは、水平スライダーコントロールで、ユーザーが現在再生中のビデオ内の任意の時間位置を動的に探すことができます。
solution: Experience Manager
title: ビデオスクラバー
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: 3e9c8800-fda2-41d1-8436-b2de7952652c
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 3%

---

# ビデオスクラバー{#video-scrubber}

ビデオスクラバは、水平スライダーコントロールで、ユーザーが現在再生中のビデオ内の任意の時間位置を動的に探すことができます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

また、ビデオの再生中にスクラバーの「ノブ」が動き、再生中にビデオの現在の時間位置を示します。 ビデオスクラバは、常にコントロールバーの幅全体を取ります。 ビデオスクラバーのスキンを適用できます。 CSSを使用して、高さと垂直方向の位置を変更します。

ビデオスクラバの一般的な外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7videoscrubber 
.s7mixedmediaviewer .s7videoscrubber .s7videotime 
.s7mixedmediaviewer .s7videoscrubber .s7knob
```

**ビデオスクラバのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む上の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む下の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバーのカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下のCSSクラスセレクターは、背景、再生および読み込みのインジケーターを追跡します。

```
.s7mixedmediaviewer .s7videoscrubber .s7track 
.s7mixedmediaviewer .s7videoscrubber .s7trackloaded 
.s7mixedmediaviewer .s7videoscrubber .s7trackplayed
```

**トラックのCSSプロパティ**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>対応するトラックの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>対応するトラックのカラー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下に示すCSSクラスセレクターで、ノブを制御します。

```
.s7mixedmediaviewer .s7videoscrubber .s7knob
```

**ノブのCSSプロパティ**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p>ノブの垂直方向のオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ノブの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>ノブの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>ノブのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下に示すCSSクラスセレクターで、再生時間の吹き出しを制御します。

```
.s7mixedmediaviewer .s7videoscrubber .s7videotime
```

**再生時間吹き出しのCSSプロパティ**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>吹き出し領域の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>吹き出し領域の高さ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>バブル領域のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>バブルのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>吹き出し領域でのテキストの整列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビデオスクラバのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

高さが10ピクセルで、コントロールバーの上および左端から10ピクセルおよび35ピクセルの位置に配置するカスタムのトラックカラーのビデオスクラバを含む混在メディアビューアを設定するには、次のように記述します。

```
.s7mixedmediaviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

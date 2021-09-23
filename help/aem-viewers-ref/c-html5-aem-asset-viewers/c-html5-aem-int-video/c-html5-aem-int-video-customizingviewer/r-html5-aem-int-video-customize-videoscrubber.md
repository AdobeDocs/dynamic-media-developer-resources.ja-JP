---
title: ビデオスクラバー
description: ビデオスクラバは、水平スライダーコントロールで、ユーザーが現在再生中のビデオ内の任意の時間位置を動的に探すことができます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9d11f2e9-315c-44d8-beb1-530d2b316604
source-git-commit: 14ca8cd5e1ce60d59806765e573e50417d0ccc50
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 2%

---

# ビデオスクラバー{#video-scrubber}

ビデオスクラバは、水平スライダーコントロールで、ユーザーが現在再生中のビデオ内の任意の時間位置を動的に探すことができます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

また、ビデオの再生中にスクラバーの「ノブ」が動き、再生中にビデオの現在の時間位置を示します。 ビデオスクラバは、常にコントロールバーの幅全体を取ります。 ビデオスクラバをスキン付けし、CSSを使用して高さと垂直方向の位置を変更できます。

ビデオスクラバの一般的な外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7videoscrubber 
.s7interactivevideoviewer .s7videoscrubber .s7videotime 
.s7interactivevideoviewer .s7videoscrubber .s7knob
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
.s7interactivevideoviewer .s7videoscrubber .s7track 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed
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
.s7interactivevideoviewer .s7videoscrubber .s7knob
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
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下に示すCSSクラスセレクターで、再生時間の吹き出しを制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7videotime
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
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>吹き出し領域でのテキストの整列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビデオスクラバのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

**例**  — ビデオスクラバーを含み、高さが10ピクセルのカスタムのトラックカラーを持つビデオビューアを設定するには、次のように記述します。コントロールバーの上端と左端から10ピクセル、左端から35ピクセルの位置に配置します。

```
.s7interactivevideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

`navigation`パラメーターでビデオチャプターマーカーを有効にすると、チャプターの位置がビデオスクラバートラックの上にマーカーとして表示されます。

ビデオチャプターマーカーは、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation
```

**ビデオチャプターマーカーのCSSプロパティ**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターマーカーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターマーカーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターマーカーのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、 `state`属性セレクターがサポートされます。このセレクターを使用して、ボタンの状態ごとに異なるスキンを適用できます。 特に、 `selected='default'`はデフォルトのビデオチャプターマーカーの状態に対応し、 `selected='over'`は、マウスを置くかタッチジェスチャによってビデオチャプターマーカーがアクティブになったときに使用されます。

**例**  - 5 x 8ピクセルで、「デフォルト」と「オーバー」状態で異なるアートを使用するビデオチャプターマーカーを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

ビデオチャプター吹き出しは、ビデオチャプターマーカーの上に配置され、特定のチャプターのタイトル、開始時間および説明を表示します。 吹き出しの幅の最大値と、ビデオスクラバートラックに対する垂直方向のオフセットを制御できます。 残りの部分は、コンポーネントによって自動的に計算されます。

ビデオチャプター吹き出しは、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter
```

**ビデオチャプター吹き出しのCSSプロパティ**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター吹き出しの最大幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバトラックからの垂直方向のオフセット。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — 幅が235ピクセルで、ビデオスクラバートラックの下端から8ピクセル上にあるビデオチャプター吹き出しを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

ビデオチャプター吹き出しは、オプションのヘッダーとコンテンツで構成されます。 ヘッダーには、オプションのチャプター開始時間とチャプタータイトルが含まれます。

ヘッダーは、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header
```

**ビデオチャプター吹き出しヘッダーのCSSプロパティ**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター吹き出しのヘッダーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター吹き出しのヘッダーテキストの内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター吹き出しのヘッダーの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行の高さ  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター吹き出しのヘッダーのテキスト行の高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — 高さが22ピクセル、線の高さが22ピクセル、水平方向のマージンが12ピクセル、背景がグレーのビデオチャプター吹き出しのヘッダーを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

ビデオチャプターの開始時間は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**ビデオチャプターの開始時間のCSSプロパティ**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>テキストカラー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right  </span> </p> </td> 
   <td colname="col2"> <p> 開始時間とチャプタータイトルの間のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — グレーの10ピクセルのVerdanaフォントを使用し、右側に10ピクセルのパディングがあるチャプター開始時間を設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

ビデオチャプタータイトルは、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**ビデオチャプタータイトルのCSSプロパティ**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのフォントファミリ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — 白、太字、10ピクセルのVerdanaフォントを使用するビデオチャプタータイトルを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

ビデオチャプターの説明は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description
```

**ビデオチャプター説明のCSSプロパティ**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明のテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明のフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明のフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明のフォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行の高さ  </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明の行の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明の内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — ダークグレーの11ピクセルのVerdanaフォントを使用し、ライトグレーの背景にビデオチャプターの説明を設定するには、次のように記述します。5ピクセルの線の高さ、12ピクセルの水平パディング、12ピクセルの上パディング、9ピクセルの下パディング。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

チャプター吹き出しの下部にあるウェッジコネクタは、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail
```

**ウェッジコネクタのCSSプロパティ**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color  </span> </p> </td> 
   <td colname="col2"> <p>ウェッジコネクタの色。 </p> <p><span class="codeph"> &lt;color&gt; transparent </span>と定義され、上の境界線の色のみが定義され、残りの境界線は透明になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width  </span> </p> </td> 
   <td colname="col2"> <p> ウェッジコネクタの幅。 </p> <p><span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span>として定義され、上と横の境界線に対してのみ同じ幅が定義され、下の境界線の幅は<span class="codeph"> 0 </span>になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 負の下余白のみを定義します。 <span class="codeph"> border-width </span>と同じ値にする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — グレーの6ピクセルのウェッジコネクタを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

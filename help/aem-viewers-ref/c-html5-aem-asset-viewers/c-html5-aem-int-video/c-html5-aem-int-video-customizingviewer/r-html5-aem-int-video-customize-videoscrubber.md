---
title: ビデオスクラバー
description: ビデオスクラバーは、ユーザーが現在再生中のビデオ内の任意の時間位置を動的に探すことができる水平スライダーコントロールです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9d11f2e9-315c-44d8-beb1-530d2b316604
source-git-commit: 14ca8cd5e1ce60d59806765e573e50417d0ccc50
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# ビデオスクラバー{#video-scrubber}

ビデオスクラバーは、ユーザーが現在再生中のビデオ内の任意の時間位置を動的に探すことができる水平スライダーコントロールです。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

スクラバーの「ノブ」も、ビデオの再生中に移動し、再生中のビデオの現在の時間位置を示します。 ビデオスクラバーは常にコントロールバーの幅全体を取ります。 CSS によって、ビデオスクラバーをスキニングし、その高さと垂直方向の位置を変更することが可能です。

ビデオスクラバーの一般的な外観は、次の CSS クラスセレクターで制御します。

```
.s7interactivevideoviewer .s7videoscrubber 
.s7interactivevideoviewer .s7videoscrubber .s7videotime 
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**ビデオスクラバーの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>上部のボーダーから配置（パディングを含む）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p> 下罫線からパディングを含めて移動します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバーの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

次の CSS クラスセレクターは、背景、再生、読み込みの指標を追跡します。

```
.s7interactivevideoviewer .s7videoscrubber .s7track 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed
```

**トラックの CSS プロパティ**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>対応するトラックの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>対応するトラックの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

次の CSS クラスセレクターでつまみを制御しています。

```
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**ノブの CSS プロパティ**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 天 </span> </p> </td> 
   <td colname="col2"> <p>垂直ノブ オフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ノブの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ノブの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>ノブ アートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

次の CSS クラスセレクターは、タイムバブルを制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7videotime
```

**バブルを再生した時間の CSS プロパティ**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>バブル領域の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>バブル領域の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>バブル領域のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>バブルアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>テキストとバブル領域の配置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビデオスクラバーツールチップは局在可能である。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

**例** - ビデオスクラバーとカスタムのトラックカラー（高さ 10 ピクセル）でビデオビューアを設定するには： コントロールバーの上端と左端から 10 ピクセル、35 ピクセルの位置を指定します。

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

`navigation` パラメーターでビデオチャプターマーカーを有効にすると、チャプターの場所がビデオスクラバートラックの上にマーカーとして表示されます。

ビデオチャプターマーカーは、次の CSS クラスセレクターで制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation
```

**ビデオチャプターマーカーの CSS プロパティ**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターマーカーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターマーカーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターマーカーのアートワーク </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合、アートワークスプライト内に配置します。 </p> <p>CSS スプライト <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> ージ </a> 参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、`state` 属性セレクターがサポートされています。このセレクターを使用して、異なるボタン状態に異なるスキンを適用できます。 特に、`selected='default'` は、デフォルトのビデオチャプターマーカーの状態に対応しており、マウスオーバーまたはタッチジェスチャーによってビデオチャプターマーカーがアクティブにされたときに `selected='over'` が使用されます。

**例** - ビデオチャプターマーカーを 5 x 8 ピクセルで、「デフォルト」と「オーバー」の状態に異なるアートを使用するように設定する

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

ビデオチャプターバブルは、ビデオチャプターマーカーの上に配置され、特定のチャプターのタイトル、開始時刻および説明を表示します。 ビデオスクラバートラックに対する最大バブル幅と垂直オフセットを制御できます。 残りは、コンポーネントによって自動的に計算されます。

ビデオチャプターバブルは、次の CSS クラスセレクターで制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter
```

**ビデオチャプターバブルの CSS プロパティ**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターバブルの最大幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバートラックからの垂直オフセット。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 幅 235 ピクセルで、ビデオスクラバートラックの下部から上に 8 ピクセルのビデオチャプターバブルを設定する場合

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

ビデオチャプターバブルは、オプションのヘッダーとコンテンツで構成されています。 ヘッダーには、オプションでチャプター開始時刻とチャプタータイトルがあります。

ヘッダーは、次の CSS クラスセレクターで制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header
```

**ビデオチャプターバブルヘッダーの CSS プロパティ**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターバブルのヘッダーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターバブルヘッダーテキストの内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターバブルヘッダーの背景色 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターバブルヘッダーのテキストの行の高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 高さが 22 ピクセル、行が 22 ピクセル、水平方向の余白が 12 ピクセル、背景がグレーのビデオチャプターバブルヘッダーを設定する

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

ビデオチャプターの開始時刻は、次の CSS クラスセレクターで制御されます。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**ビデオチャプター開始時刻の CSS プロパティ**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>テキストのカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>フォントの線幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right </span> </p> </td> 
   <td colname="col2"> <p> 開始時間とチャプタータイトルの間のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - グレーの 10 ピクセルの Verdana フォントを使用し、右側に 10 ピクセルのパディングを持つチャプター開始時刻を設定します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

ビデオのチャプタータイトルは、次の CSS クラスセレクターで制御されます。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**ビデオチャプタータイトルの CSS プロパティ**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのフォントファミリー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 白、太字、10 ピクセルの Verdana フォントを使用するビデオチャプターのタイトルを設定します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

ビデオのチャプターの説明は、次の CSS クラスセレクターで制御されます。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description
```

**ビデオチャプター説明の CSS プロパティ**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターの説明のテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターの説明背景色 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターの説明のフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明のフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターの説明フォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターの説明の行の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターの説明内部パディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - 11 ピクセルのダークグレーの Verdana フォントを使用し、背景をライトグレーにして、ビデオチャプターの説明を設定します。 行の高さが 5 ピクセル、水平方向の余白が 12 ピクセル、上の余白が 12 ピクセル、下の余白が 9 ピクセルです。

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

チャプターバブルの下部にあるくさびコネクタは、次の CSS クラスセレクターで制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail
```

**ウェッジコネクタの CSS プロパティ**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>くさびコネクタの色。 </p> <p>上の境界線 <span class="codeph"> 色のみが定義され、残りの境界線は透明になるように、&lt;color&gt; 透明 </span> として定義されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> ウェッジコネクタの幅。 </p> <p><span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> として定義されているため、同じ幅が上と横の境界線に対してのみ定義され、下の境界線の幅は <span class="codeph"> 0 </span> になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 負の下余白のみを定義します。 border-width <span class="codeph"> と同じ値 </span> 指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - グレーの 6 ピクセルのくさびコネクタを設定するには：

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

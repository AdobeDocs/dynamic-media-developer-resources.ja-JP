---
title: ビデオスクラバ
description: ビデオスクラバは、水平方向のスライダーコントロールで、現在再生中のビデオ内の任意の時点をユーザーが動的に探すことができます
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 2%

---

# ビデオスクラバ{#video-scrubber}

ビデオスクラバは、水平方向のスライダーコントロールで、現在再生中のビデオ内の任意の時点をユーザーが動的にシークできます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

また、ビデオの再生中にスクラバー「ノブ」が移動し、再生中のビデオの現在の時間位置を示します。 ビデオスクラバは、常にコントロールバーの幅全体になります。 ビデオスクラバにスキンを適用し、CSS を使用して高さと垂直方向の位置を変更できます。

ビデオスクラバの一般的な外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**ビデオスクラバーの CSS プロパティ**

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバーの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下の CSS クラスセレクターは、背景、再生および読み込みのインジケーターを追跡します。

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**トラックの CSS プロパティ**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>対応するトラックの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>対応するトラックの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下に示す CSS クラスセレクターで、ノブを制御します。

```
.s7videoviewer .s7videoscrubber .s7knob
```

**ノブの CSS プロパティ**

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
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ノブの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>ノブのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

以下に示す CSS クラスセレクターで、再生時間の吹き出しを制御します。

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**再生時間の吹き出しの CSS プロパティ**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントサイズです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>吹き出し領域の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>吹き出し領域の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>吹き出し領域のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>バブルのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>吹き出し領域でのテキストの整列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビデオスクラバのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

**例**  — カスタムのトラックカラーを持つビデオスクラバを持つビデオビューアを設定するには、次の手順を実行します。 スクラバは、高さが 10 ピクセルで、コントロールバーの上および左端から 10 ピクセルおよび 35 ピクセルの位置に配置する必要があります。

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

ビデオチャプターが `navigation` パラメーターを指定すると、チャプターの位置がマーカーとしてビデオスクラバートラックの上に表示されます。

ビデオチャプターマーカーは、以下の CSS クラスセレクターを使用して制御します。

```
 .s7videoviewer .s7videoscrubber .s7navigation
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
   <td colname="col2"> <p>ビデオチャプターマーカーのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に `selected='default'` は、デフォルトのビデオチャプターマーカーの状態に対応し、 `selected='over'` は、マウスを合わせるかタッチジェスチャによってビデオチャプターマーカーがアクティブになった場合に使用されます。

**例** - 5 x 8 ピクセルで、「デフォルト」と「オーバー」の状態で異なるアートを使用するビデオチャプターマーカーを設定するには。

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

ビデオチャプター吹き出しは、ビデオチャプターマーカーの上に配置され、特定のチャプターのタイトル、開始時間および説明を表示します。 吹き出しの幅の最大値と、ビデオスクラバートラックに対する垂直方向のオフセットを制御できます。 残りの部分は、コンポーネントによって自動的に計算されます。

ビデオチャプター吹き出しは、以下の CSS クラスセレクターを使用して制御します。

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**ビデオチャプター吹き出しの CSS プロパティ**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター吹き出しの最大幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバートラックからの垂直方向のオフセット。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — 幅が 235 ピクセルで、ビデオスクラバートラックの下部から 8 ピクセル上にあるビデオチャプター吹き出しを設定するには、次のように記述します。

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

ビデオチャプター吹き出しは、オプションのヘッダーとコンテンツで構成されます。 ヘッダーには、オプションのチャプター開始時間とチャプタータイトルが含まれます。

ヘッダーは、以下の CSS クラスセレクターを使用して制御します。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**ビデオチャプター吹き出しヘッダーの CSS プロパティ**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター吹き出しのヘッダーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター吹き出しのヘッダーテキストの内側のパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター吹き出しのヘッダーの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行の高さ </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター吹き出しのヘッダーテキストの行の高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — 高さが 22 ピクセル、線の高さが 22 ピクセル、水平方向のマージンが 12 ピクセル、背景がグレーのビデオチャプター吹き出しのヘッダーを設定するには、次のように記述します。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

ビデオチャプターの開始時間は、以下の CSS クラスセレクターを使用して制御します。

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**ビデオチャプターの開始時間の CSS プロパティ**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー </span> </p> </td> 
   <td colname="col2"> <p>テキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right </span> </p> </td> 
   <td colname="col2"> <p> 開始時間とチャプタータイトルの間のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — グレーの 10 ピクセル Verdana フォントを使用し、右側に 10 ピクセルのパディングを持つチャプター開始時間を設定するには、次の手順を実行します。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

ビデオチャプタータイトルは、以下の CSS クラスセレクターを使用して制御します。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**ビデオチャプタータイトルの CSS プロパティ**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプタータイトルのフォントファミリ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — 白、太字、10 ピクセルの Verdana フォントを使用するビデオチャプタータイトルを設定するには、次の手順を実行します。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

ビデオチャプターの説明は、以下の CSS クラスセレクターを使用して制御します。

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

**ビデオチャプターの説明の CSS プロパティ**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明のテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明のフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明のフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明のフォントファミリ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行の高さ </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明の行の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプター説明の内側のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — ダークグレーの 11 ピクセルの Verdana フォントを使用し、ライトグレーの背景を持つビデオチャプターの説明を設定するには、次の手順を実行します。 最後に、は、5 ピクセルの線の高さ、12 ピクセルの水平パディング、12 ピクセルの上パディング、9 ピクセルの下パディングを使用します。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

チャプター吹き出しの下部にあるウェッジコネクタは、以下の CSS クラスセレクターを使用して制御します。

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**ウェッジコネクタの CSS プロパティ**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>ウェッジコネクタの色。 </p> <p>次のように定義： <span class="codeph"> &lt;color&gt; 透明 </span> 上の境界線の色のみを定義し、残りの境界線は透明になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> ウェッジコネクタの幅。 </p> <p>次のように定義： <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> 上と横の境界線に対してのみ同じ幅を定義し、下の境界線の幅は <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 負の下余白のみを定義します。 と同じ値にする必要があります。 <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**例**  — グレーの 6 ピクセルのウェッジコネクタを設定するには：

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

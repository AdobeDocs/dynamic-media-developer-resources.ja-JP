---
title: ビデオスクラバー
description: ビデオスクラバーは、現在再生中のビデオ内の任意の時間の位置を動的に探すことができる水平スライダーコントロールです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9d11f2e9-315c-44d8-beb1-530d2b316604
TQID: 'https://experienceleague.adobe.com/XLrCMFCLFFTSX4dvx84u0LeR-46CRfyzkTNQuWSlwk0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1063
ht-degree: 0%

---

# ビデオスクラバー{#video-scrubber}

ビデオスクラバーは、現在再生中のビデオ内の任意の時間の位置を動的に探すことができる水平スライダーコントロールです。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

スクラバー「ノブ」は、再生中にビデオの現在の時間位置を示すために、ビデオの再生に合わせて移動します。 ビデオスクラバーは常にコントロールバーの幅全体を取ります。 ビデオスクラバーをスキンし、CSSによってその高さと垂直位置を変更することが可能です。

ビデオスクラバーの一般的な外観は、次のCSS クラスセレクターで制御されます。

```
.s7interactivevideoviewer .s7videoscrubber 
.s7interactivevideoviewer .s7videoscrubber .s7videotime 
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

ビデオスクラバーの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p>パディングを含む上部境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p> パディングを含む下部境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラバーの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

次のCSS クラスセレクターは、背景、再生、読み込みのインジケーターを追跡します。

```
.s7interactivevideoviewer .s7videoscrubber .s7track 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed
```

トラックの&#x200B;**CSS プロパティ**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>対応するトラックの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>対応するトラックの色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

次のCSS クラスセレクターは、ノブを制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

ノブの&#x200B;**CSS プロパティ**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p>垂直ノブオフセット </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ノブの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ノブの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>ノブのアートワーク： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

次のCSS クラスセレクターは、再生時間バブルを制御します。

```
.s7interactivevideoviewer .s7videoscrubber .s7videotime
```

バブル再生時間の&#x200B;**CSS プロパティ**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p> 時間表示テキストに使用するフォントカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>バブル領域の幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>バブル領域の高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>バブル領域のパディング </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>バブルアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> テキスト整列</span> </p> </td> 
   <td colname="col2"> <p>バブル領域でのテキストの整列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビデオスクラバーのツールチップはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

**例** – 高さ10 ピクセルのカスタムトラックカラーを使用して、ビデオスクラバーを使用したビデオビューアを設定します。 コントロールバーの上端と左端から10 ピクセルと35 ピクセルを配置します。

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

`navigation` パラメーターでビデオチャプターマーカーを有効にすると、チャプターの場所がビデオスクラブラートラックの上にマーカーとして表示されます。

ビデオチャプターマーカーは、次のCSS クラスセレクターによって制御されます。

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation
```

ビデオ チャプターマーカー&#x200B;**の** CSS プロパティ

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターマーカーの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターマーカーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章マーカーアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。 特に、`selected='default'`はデフォルトのビデオチャプターマーカーの状態に対応し、`selected='over'`はマウスオーバーまたはタッチジェスチャーによってビデオチャプターマーカーがアクティブ化されたときに使用されます。

**例** - 5 x 8 ピクセルのビデオチャプターマーカーを設定し、「デフォルト」状態と「オーバー」状態に異なるアートを使用するには、次の手順を実行します。

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

ビデオチャプターバブルは、ビデオチャプターマーカーの上に配置され、特定のチャプターのタイトル、開始時間、説明を表示します。 ビデオスクラブトラックに対する最大バブル幅と垂直オフセットを制御できます。 残りはコンポーネントによって自動的に計算されます。

ビデオチャプターのバブルは、次のCSS クラスセレクターによって制御されます。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter
```

**ビデオチャプターバブルのCSS プロパティ**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p>ビデオチャプターバブルの最大幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p>ビデオスクラブトラックからの垂直オフセット。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 幅235 ピクセル、ビデオスクラバートラックの下部から上に8 ピクセルのビデオチャプターバブルを設定します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

ビデオチャプターのバブルは、オプションのヘッダーとコンテンツで構成されます。 ヘッダーには、オプションの章の開始時間と章のタイトルがあります。

ヘッダーは、次のCSS クラスセレクターによって制御されます。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header
```

**ビデオ章の吹き出しヘッダーのCSS プロパティ**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章のバブル ヘッダーの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>ビデオの章の吹き出しヘッダーテキストのインナーパディング。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章の吹き出しのヘッダーの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行の高さ</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章の吹き出しヘッダーテキストの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 高さ22 ピクセル、高さ22 ピクセル、水平方向の余白12 ピクセル、グレーの背景を持つビデオチャプターのバブルヘッダーを設定するには、次の手順を実行します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

ビデオチャプターの開始時間は、次のCSS クラスセレクターによって制御されます。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

ビデオチャプターの&#x200B;**CSS プロパティ開始時間**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>テキストの色： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>フォントの太さ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォントファミリー： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング右</span> </p> </td> 
   <td colname="col2"> <p> 開始時間と章タイトルの間のパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 灰色の10 ピクセルのVerdana フォントを使用して章の開始時間を設定し、10 ピクセルが右側にパディングされます。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

ビデオチャプターのタイトルは、次のCSS クラスセレクターによって制御されます。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

ビデオ章タイトルの&#x200B;**CSS プロパティ**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章タイトルのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章タイトルのフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>ビデオ章タイトルのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章タイトルのフォントファミリー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 白、太字、10 ピクセルのVerdana フォントを使用するビデオ章タイトルを設定します。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

ビデオチャプターの説明は、次のCSS クラスセレクターによって制御されます。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description
```

ビデオチャプターの説明&#x200B;**CSS プロパティ**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章の説明テキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章の説明の背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章の説明フォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>ビデオ章の説明フォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章説明フォントファミリー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行の高さ</span> </p> </td> 
   <td colname="col2"> <p>ビデオ章の説明ラインの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パディング </span> </p> </td> 
   <td colname="col2"> <p>ビデオ章の説明インナーパディング。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** – 明るいグレーの背景を持つ、ダークグレーの11 ピクセルのVerdana フォントを使用してビデオチャプターの説明を設定します。 5 ピクセルの行高さ、12 ピクセルの水平パディング、12 ピクセルの上パディング、および9 ピクセルの下パディング。

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

チャプターバブルの下部にあるウェッジコネクタは、次のCSS クラスセレクターによって制御されます。

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail
```

ウェッジコネクタの&#x200B;**CSS プロパティ**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>ウェッジコネクタの色。 </p> <p><span class="codeph"> &lt;color&gt;透明</span>として定義して、上の境界線の色のみが定義され、残りの境界線は透明のままにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> ウェッジコネクタの幅。 </p> <p><span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span>として定義され、同じ幅が上と横の境界線にのみ定義され、下の境界線の幅が<span class="codeph"> 0 </span>になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p> 負の下余白のみを定義します。 これは、<span class="codeph"> border-width </span>と同じ値である必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**例** - グレーの6 ピクセルのウェッジコネクタを設定するには：

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

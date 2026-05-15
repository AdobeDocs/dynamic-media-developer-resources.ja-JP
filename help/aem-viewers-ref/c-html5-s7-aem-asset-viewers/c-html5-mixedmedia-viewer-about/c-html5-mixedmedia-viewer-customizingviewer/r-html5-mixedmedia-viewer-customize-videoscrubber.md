---
title: ビデオスクラバー
description: ビデオスクラバーは、現在再生中のビデオ内の任意の時間の位置を動的に探すことができる水平スライダーコントロールです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3e9c8800-fda2-41d1-8436-b2de7952652c
TQID: 'https://experienceleague.adobe.com/2RuNN74vMpWIzTg3QGXNdPWlnWIAIobpXiplimAHsAw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 369
ht-degree: 0%

---

# ビデオスクラバー{#video-scrubber}

ビデオスクラバーは、現在再生中のビデオ内の任意の時間の位置を動的に探すことができる水平スライダーコントロールです。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

スクラバー「ノブ」は、再生中にビデオの現在の時間位置を示すために、ビデオの再生に合わせて移動します。 ビデオスクラバーは常にコントロールバーの幅全体を取ります。 CSSを使用して、ビデオスクラバーのスキンを作成し、その高さと垂直位置を変更することができます。

ビデオスクラバーの一般的な外観は、次のCSS クラスセレクターで制御されます。

```
.s7mixedmediaviewer .s7videoscrubber 
.s7mixedmediaviewer .s7videoscrubber .s7videotime 
.s7mixedmediaviewer .s7videoscrubber .s7knob
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
.s7mixedmediaviewer .s7videoscrubber .s7track 
.s7mixedmediaviewer .s7videoscrubber .s7trackloaded 
.s7mixedmediaviewer .s7videoscrubber .s7trackplayed
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
.s7mixedmediaviewer .s7videoscrubber .s7knob
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

次のCSS クラスセレクターは、再生時間バブルを制御します。

```
.s7mixedmediaviewer .s7videoscrubber .s7videotime
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
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> テキスト整列</span> </p> </td> 
   <td colname="col2"> <p>バブル領域でのテキストの整列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

ビデオスクラバーのツールチップはローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

高さ10 ピクセルのカスタムトラックカラーを持ち、コントロールバーの上端と左端から10 ピクセルと35 ピクセルに配置されたビデオスクラバーを使用して、混在メディアビューアを設定します。

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

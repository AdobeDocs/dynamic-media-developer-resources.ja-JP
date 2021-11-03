---
title: ビデオプレーヤー
description: スマート切り抜きビデオプレーヤーは、ビューア内でビデオコンテンツが表示される長方形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2741821f-78fe-44d4-8604-fee10086e0a0
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 1%

---

# ビデオプレーヤー{#video-player}

スマート切り抜きビデオプレーヤーは、ビューア内でビデオコンテンツが表示される長方形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生中のビデオのサイズがスマート切り抜きビデオプレーヤーのサイズと一致しない場合、ビデオコンテンツはスマート切り抜きビデオプレーヤーの長方形の表示領域内に中央揃えになります。

以下に示す CSS クラスセレクターで、スマート切り抜きビデオプレーヤーの外観を制御します。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**スマート切り抜きビデオプレーヤーの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>メインビューの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

システムでビデオを再生できない場合に表示されるエラーメッセージをローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 — スマート切り抜きビデオプレーヤーのサイズが 512 x 288 ピクセルに設定されたスマート切り抜きビデオビューアを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

クローズドキャプションは、スマート切り抜きビデオプレーヤー内の内部コンテナに配置されます。 そのコンテナの位置は、サポートされている WebVTT の位置決め演算子で制御します。 キャプションテキスト自体はコンテナ内にあり、そのスタイルは以下の CSS クラスセレクターを使用して制御します。

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**クローズドキャプションの CSS プロパティ**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションのテキストの背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションのテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p> クローズドキャプションのフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> クローズドキャプションのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションのフォント。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 14 ピクセル、ライトグレー、Arial®の、半透明の黒い背景にクローズドキャプションのテキストを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

バッファリングアニメーションの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
```

**待機アイコンの CSS プロパティ**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの左余白（通常はアイコンの幅の半分を引いたもの）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの上余白（通常はアイコンの高さの半分を引いた値）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> ノブのアートワーク。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が 101 ピクセル、高さが 29 ピクセルのバッファリングアニメーションを設定するには、次のように記述します。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

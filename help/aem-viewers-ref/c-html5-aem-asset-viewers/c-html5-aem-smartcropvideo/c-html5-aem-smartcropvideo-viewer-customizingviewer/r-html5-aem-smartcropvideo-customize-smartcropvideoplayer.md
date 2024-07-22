---
title: ビデオプレーヤー
description: スマート切り抜きビデオプレーヤーは、ビューア内でビデオコンテンツが表示される長方形の領域です。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# ビデオプレーヤー{#video-player}

スマート切り抜きビデオプレーヤーは、ビューア内でビデオコンテンツが表示される長方形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生中のビデオのサイズがスマート切り抜きビデオプレーヤーのサイズと一致しない場合、ビデオコンテンツは、スマート切り抜きビデオプレーヤーの長方形表示領域の中央に配置されます。

次の CSS クラスセレクターは、スマート切り抜きビデオプレーヤーの外観を制御します。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**スマート切り抜きビデオプレーヤーの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>メインビューの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

システムがビデオを再生できない場合に表示されるエラーメッセージをローカライズできます。 詳しくは、[ ユーザーインターフェイス要素のローカライゼーション ](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) を参照してください。

例 – スマート切り抜きビデオプレーヤーサイズを 512 x 288 ピクセルに設定してスマート切り抜きビデオビューアを設定する

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

クローズドキャプションは、スマート切り抜きビデオプレーヤー内の内部コンテナに配置されます。 そのコンテナの位置は、サポートされる WebVTT 位置決め演算子で制御されます。 キャプションテキスト自体はそのコンテナ内にあり、そのスタイルは次の CSS クラスセレクターで制御されます。

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**クローズドキャプションの CSS プロパティ**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションテキストの背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>字幕のテキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの太さの </span> </p> </td> 
   <td colname="col2"> <p> 字幕のフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> クローズドキャプションのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>字幕フォント。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – クローズドキャプションのテキストを 14 ピクセル、薄いグレー、Arial® の半透明の黒い背景に設定する場合：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

バッファリングアニメーションの外観は、次の CSS クラスセレクターで制御します。

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
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p> アニメーション アイコンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの左余白。通常は、アイコンの幅の半分を引きます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> アニメーション アイコン上余白（通常はアイコンの高さの半分を引いた値） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> ノブ アートワーク。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 幅 101 ピクセル、高さ 29 ピクセルのバッファリングアニメーションを設定するには：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

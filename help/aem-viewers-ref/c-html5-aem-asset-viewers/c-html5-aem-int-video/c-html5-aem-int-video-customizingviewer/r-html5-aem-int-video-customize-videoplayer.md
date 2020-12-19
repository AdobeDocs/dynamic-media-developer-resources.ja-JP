---
description: ビデオプレーヤーは、ビューア内でビデオコンテンツが表示される矩形の領域です。
seo-description: ビデオプレーヤーは、ビューア内でビデオコンテンツが表示される矩形の領域です。
seo-title: ビデオプレーヤー
solution: Experience Manager
title: ビデオプレーヤー
topic: Dynamic media
uuid: ff0f78b1-ff88-47b8-a118-4e0b3e75f341
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 1%

---


# ビデオプレーヤー{#video-player}

ビデオプレーヤーは、ビューア内でビデオコンテンツが表示される矩形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生中のビデオのサイズがビデオプレーヤーのサイズと一致しない場合、ビデオコンテンツはビデオプレーヤーの矩形の表示領域内に中央配置されます。

以下に示すCSSクラスセレクターで、ビデオプレーヤーの外観を制御します。

```
.s7interactivevideoviewer .s7videoplayer
```

**ビデオプレーヤーのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>メイン表示の背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

システムでビデオを再生できない場合に表示されるエラーメッセージをローカライズできます。

[ユーザインターフェイス要素のローカライゼーション](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 — サイズが512 x 288ピクセルのビデオプレーヤーを持つビデオビューアを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

クローズドキャプションは、ビデオプレーヤー内部のコンテナに配置されます。 そのコンテナの位置は、サポートされているWebVTT位置決め演算子で制御します。 キャプションテキスト自体はそのコンテナ内にあり、そのスタイルは以下のCSSクラスセレクターを使用して制御します。

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**クローズドキャプションのCSSプロパティ**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションのテキストの背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションのテキストカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-重み付け  </span> </p> </td> 
   <td colname="col2"> <p> クローズドキャプションのフォント重み付け。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> クローズドキャプションのフォントサイズ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションのフォント。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-5b82913ff3c44b7b8187969cb15e9560}

クローズドキャプションのテキストが14ピクセル、ライトグレー、Arialで、背景色が半透明の黒であるように設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

バッファリングアニメーションの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
```

**待機アイコンのCSSプロパティ**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSSプロパティ </p> </th> 
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
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの左マージン。通常はアイコンの幅の半分を引いた値。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの上余白。通常はアイコンの高さの半分を引いた値です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> ノブのアートワーク。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が101ピクセル、高さが29ピクセルのバッファリングアニメーションを設定するには、次のように記述します。

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```


---
title: ビデオプレーヤー
description: スマート切り抜きビデオプレーヤーは、ビデオコンテンツがビューア内に表示される長方形の領域です。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
autotag-review: '2026-05-13T22:20:27.128Z'
TQID: 'https://experienceleague.adobe.com/rIAk03o-xH-YQkln2YFJfSKqxoTK0ziIXG86NgrlJnM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 328
ht-degree: 0%

---

# ビデオプレーヤー{#video-player}

スマート切り抜きビデオプレーヤーは、ビデオコンテンツがビューア内に表示される長方形の領域です。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

再生するビデオのサイズがスマート切り抜きビデオプレーヤーのサイズと一致しない場合、ビデオコンテンツはスマート切り抜きビデオプレーヤーの長方形の表示領域内に配置されます。

次のCSS クラスセレクターは、スマート切り抜きビデオプレーヤーの外観を制御します。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

スマート切り抜きビデオプレーヤーの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>メインビューの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

システムがビデオを再生できない場合に表示されるエラーメッセージは、ローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)を参照してください。

例 – スマート切り抜きビデオプレーヤーのサイズが512 x 288 ピクセルに設定されたスマート切り抜きビデオビューアを設定する場合。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

クローズドキャプションは、スマート切り抜きビデオプレーヤー内の内部コンテナに入れられます。 そのコンテナの位置は、サポートされているWebVTT ポジショニングオペレーターによって制御されます。 キャプションテキスト自体はそのコンテナ内にあり、そのスタイルは次のCSS クラスセレクターで制御されます。

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

クローズドキャプションの&#x200B;**CSS プロパティ**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションテキストの背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> カラー</span> </p> </td> 
   <td colname="col2"> <p>キャプションテキストの色を閉じます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントの重み</span> </p> </td> 
   <td colname="col2"> <p> クローズドキャプションのフォントの太さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p> クローズドキャプションのフォントサイズ： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>クローズドキャプションのフォント。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 半透明の黒い背景に、クローズドキャプションテキストを14 ピクセル、ライトグレー、Arial®に設定するには：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

バッファリングアニメーションの外観は、次のCSS クラスセレクターで制御されます。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
```

待機アイコン **の** CSS プロパティ

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの左余白。通常は、アイコンの幅の半分を引きます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> アニメーションアイコンの上余白（通常はアイコンの高さの半分を差し引く）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> ノブのアートワーク： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – バッファリングアニメーションを幅101 ピクセル、高さ29 ピクセルに設定するには、次の手順を実行します。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

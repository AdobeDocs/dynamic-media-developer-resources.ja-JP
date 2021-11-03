---
description: スマート切り抜きビデオビューアの JavaScript API リファレンス
solution: Experience Manager
title: setVideo
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: c89099f6-09f7-4d81-939e-90ffa2764c8c
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# setVideo{#setvideo}

スマート切り抜きビデオビューアの JavaScript API リファレンス

`setVideo(videoUrl[, data])`

新しい外部ビデオとオプションの追加ビデオデータを設定します。 いつでも呼び出すことができます（前後） `init()`. の後に呼び出された場合 `init()`を指定した場合、ビューアは実行時にビデオを入れ替えます。

関連トピック [init]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## パラメータ {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 文字列 </span>} 新しいビデオの絶対 URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> データ </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} 次のオプションフィールドを含む JSON オブジェクト（大文字と小文字が区別されます）: </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 事後的な </span>  — ビデオの再生開始前の最初のフレームに表示する画像。 詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> caption </span>  — 新しいキャプションファイルの場所。 キャプションファイルが指定されていない場合、キャプションボタンはユーザーインターフェイスに表示されません。 </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> ナビゲーション </span> - WebVTT ナビゲーションコンテンツの URL またはパス。 WebVTT ファイルは画像サービングから提供される必要があります。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```

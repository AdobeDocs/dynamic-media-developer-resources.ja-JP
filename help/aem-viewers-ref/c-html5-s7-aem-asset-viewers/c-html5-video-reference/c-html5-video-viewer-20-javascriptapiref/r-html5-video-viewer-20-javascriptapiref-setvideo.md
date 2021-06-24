---
description: ビデオビューアのJavaScript APIリファレンス
solution: Experience Manager
title: setVideo
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ
role: Developer,Business Practitioner
exl-id: c89099f6-09f7-4d81-939e-90ffa2764c8c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---

# setVideo{#setvideo}

ビデオビューアのJavaScript APIリファレンス

`setVideo(videoUrl[, data])`

新しい外部ビデオとオプションの追加ビデオデータを設定します。 `init()`の前後いつでも呼び出すことができます。 `init()`の後に呼び出した場合、ビューアは実行時にビデオを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)も参照してください。

## パラメータ {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>}新しいビデオの絶対URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> データ </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSONオブジェクト（次のオプションフィールドを含む）（大文字と小文字が区別されます）。 </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage  </span>  — ビデオの再生開始前に、最初のフレームに表示する画像。<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>を参照してください。 </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> caption - </span> 新しいキャプションファイルの場所。キャプションファイルを指定しない場合、キャプションボタンはユーザーインターフェイスに表示されません。 </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> ナビゲ </span> ーション — WebVTTナビゲーションコンテンツのURLまたはパス。WebVTTファイルは画像サービングから提供される必要があります。 </li> 
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

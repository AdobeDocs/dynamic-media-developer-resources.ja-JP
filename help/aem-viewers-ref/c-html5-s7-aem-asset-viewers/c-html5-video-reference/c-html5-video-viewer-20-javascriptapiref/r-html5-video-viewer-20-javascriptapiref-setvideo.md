---
title: setVideo
description: ビデオビューア用のJavaScript API リファレンス
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c89099f6-09f7-4d81-939e-90ffa2764c8c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# setVideo{#setvideo}

ビデオビューア用のJavaScript API リファレンス

`setVideo(videoUrl[, data])`

新しい外部ビデオとオプションの追加ビデオデータを設定します。 `init()` の前と後の両方でいつでも呼び出すことができます。 `init()` 後に呼び出された場合、ビューアは実行時にビデオをスワップします。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6) も参照してください。

## パラメーター {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} 新しいビデオへの絶対 URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> data </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} 次のオプションフィールドを含む JSON オブジェクト（大文字と小文字を区別）: </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage </span> - ビデオの再生が開始される前に、最初のフレームに表示する画像。 VideoPlayer.posterimage の </a> キュメント <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> 参照してください。 </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> caption </span> – 新しいキャプションファイルの場所。 キャプションファイルが指定されていない場合、「キャプション」ボタンはユーザーインターフェイスに表示されません。 </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> ナビゲーション </span> - WebVTT ナビゲーションコンテンツの URL またはパス。 WebVTT ファイルは、画像サービングで提供される必要があります。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```

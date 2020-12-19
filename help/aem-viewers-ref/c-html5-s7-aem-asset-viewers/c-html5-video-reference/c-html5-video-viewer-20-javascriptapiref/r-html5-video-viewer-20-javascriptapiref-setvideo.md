---
description: ビデオビューアのJavaScript APIリファレンス
seo-description: ビデオビューアのJavaScript APIリファレンス
seo-title: setVideo
solution: Experience Manager
title: setVideo
topic: Dynamic media
uuid: 0a1b3caa-ded6-4020-962c-41c3ece0a865
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# setVideo{#setvideo}

ビデオビューアのJavaScript APIリファレンス

`setVideo(videoUrl[, data])`

新しい外部ビデオおよびオプションの追加ビデオデータを設定します。 `init()`の前後いつでも呼び出すことができます。 `init()`の後に呼び出すと、ビューアは実行時にビデオを入れ替えます。

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
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSONオブジェクトと次のオプションのフィールド（大文字と小文字が区別されます）: </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> ポスタリメ </span> ージ — ビデオ開始の再生前の最初のフレームに表示する画像。<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>を参照してください。 </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> caption  </span>  — 新しいキャプションファイルの場所。キャプションファイルを指定しない場合、キャプションボタンはユーザーインターフェイスに表示されません。 </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> navigation  </span> - WebVTTナビゲーションコンテンツのURLまたはパス。WebVTTファイルは、画像サービングから提供されます。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```


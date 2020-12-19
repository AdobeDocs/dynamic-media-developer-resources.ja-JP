---
description: ビデオビューアのJavaScript APIリファレンス。
seo-description: ビデオビューアのJavaScript APIリファレンス。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 7543126c-5cc3-4010-ad7f-8d2e8d643133
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# setAsset{#setasset}

ビデオビューアのJavaScript APIリファレンス。

`setAsset(asset[, data])`

新しいアセットとオプションの追加アセットデータを設定します。 このパラメーターは、`init()`の前後いつでも呼び出すことができます。 `init()`の後に呼び出した場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)も参照してください。

## パラメータ {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">文字列</span>}の新しいアセットID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> データ </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSONオブジェクトと次のオプションのフィールド（大文字と小文字が区別されます）: </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> ポスタリメ </span> ージ — ビデオ開始の再生前の最初のフレームに表示する画像。<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>を参照してください。 </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> caption  </span>  — 新しいクローズドキャプションファイルの場所。ファイルを指定しない場合、クローズドキャプションボタンはユーザーインターフェイスに表示されません。 </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> navigation  </span> - WebVTTナビゲーションコンテンツのURLまたはパス。WebVTTファイルは、画像サービングから提供される必要があります </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```


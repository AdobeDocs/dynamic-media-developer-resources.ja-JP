---
title: setAsset
description: ビデオビューア用JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
TQID: 'https://experienceleague.adobe.com/L1FDHZnfLnN11BdkFgEvlBEdAbGIfoFT2uh3E0MnjzU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 127
ht-degree: 1%

---

# setAsset{#setasset}

ビデオビューア用JavaScript API リファレンス。

`setAsset(asset[, data])`

新しいアセットとオプションの追加アセットデータを設定します。 このパラメーターは、`init()`の前または後に、いつでも呼び出すことができます。 `init()`の後に呼び出された場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)も参照してください。

## パラメーター {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> アセット </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">文字列</span>}の新しいアセット ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> データ </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSON オブジェクトと、次のオプションフィールド（大文字と小文字を区別します）: </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> ポスター画像</span> - ビデオの再生を開始する前に、最初のフレームに表示する画像。 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>を参照してください。 </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> キャプション </span> – 新しいクローズドキャプションファイルの場所。 ファイルが指定されていない場合、クローズドキャプションボタンはユーザーインターフェイスに表示されません。 </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> ナビゲーション </span> - WebVTT ナビゲーション コンテンツのURLまたはパス。 WebVTT ファイルは、画像サービングによって提供されます </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```

---
description: スマート切り抜きビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# setAsset{#setasset}

スマート切り抜きビデオビューアの JavaScript API リファレンス。

`setAsset(asset[, data])`

新しいアセットとオプションの追加アセットデータを設定します。 このパラメーターは、いつでも（前後に）呼び出すことができます `init()`. 次の後に呼び出された場合 `init()`を指定した場合、ビューアは実行時にアセットをスワップします。

関連トピック [init]
(../././c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref\r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## パラメータ {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 文字列 </span>} 個の新しいアセット ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> データ </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} 次のオプションフィールドを含む JSON オブジェクト（大文字と小文字が区別されます）: </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 事後的な </span>  — ビデオの再生開始前の最初のフレームに表示する画像。 詳しくは、 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-cmdref/r-html5-aem-smartcropvideo-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> caption </span>  — 新しいクローズドキャプションファイルの場所。 ファイルが指定されていない場合、クローズドキャプションボタンはユーザーインターフェイスに表示されません。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```

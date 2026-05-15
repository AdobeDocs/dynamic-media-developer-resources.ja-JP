---
title: setAsset
description: インタラクティブビデオビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 24d8d11d-4688-4ca0-92ae-824a5e984a10
TQID: 'https://experienceleague.adobe.com/jht0-Zs20gbS0drsbBnYAf4wFpVbZfv2CWhIsSGEil8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 142
ht-degree: 1%

---

# setAsset{#setasset}

インタラクティブビデオビューアのJavaScript API リファレンス。

`setAsset(asset[, data])`

新しいアセットとオプションの追加アセットデータを設定します。 このパラメーターは、`init()`の前または後に、いつでも呼び出すことができます。 `init()`の後に呼び出された場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> アセット </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">文字列</span>&rbrace;の新しいアセット ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> データ </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> JSON </span>} JSON オブジェクトと、次のオプションフィールド（大文字と小文字を区別します）: </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> ポスター画像</span> - ビデオの再生を開始する前に、最初のフレームに表示する画像。 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>を参照してください。 </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> キャプション </span> – 新しいキャプションファイルの場所。 指定しない場合、キャプションボタンはユーザーインターフェイスに表示されません。 </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> ナビゲーション </span> - WebVTT ナビゲーション コンテンツのURLまたはパス。 WebVTT ファイルは、画像サービングによって提供されます。 </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interactiveData </span> - WebVTT インタラクティブデータコンテンツのURLまたはパス。 WebVTT ファイルは、画像サービングで提供する必要があります。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```

---
description: 混在メディアビューアのJavaScript APIリファレンス。
seo-description: 混在メディアビューアのJavaScript APIリファレンス。
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 8c341a8a-25b5-4db9-ad1a-919ded79f2ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---


# setAsset{#setasset}

混在メディアビューアのJavaScript APIリファレンス。

` setAsset( *`asset`*[,data]))`

新しいアセットとオプションの追加アセットデータを設定します。 このパラメーターは、`init()`の前後いつでも呼び出すことができます。 `init()`の後に呼び出した場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)も参照してください。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`asset`*`  - { `String`}新しいアセットIDまたは明示的な混在メディアセット。オプションとして画像サービング修飾子を後に付加 `?`。

IR（画像レンダリング）またはUGC（ユーザ生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

` *`data`*` - {  `JSON`}新しいキャプションファイルの場所。

指定しなかった場合、キャプションボタンはユーザーインターフェイスに表示されません。 このパラメーターで指定されたキャプションは、混在メディアセットでの最初のビデオに適用されます。後続のビデオはキャプションなしで再生されます。 このビューアでは、次のコンポーネントIDがサポートされています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネントID </p> </th> 
   <th colname="col2" class="entry"> <p>ビューアSDKコンポーネントのクラス名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage  </span> </p> </td> 
   <td colname="col2"> <p>ビデオ開始の再生前の最初のフレームに表示する画像。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> caption  </span> </p> </td> 
   <td colname="col2"> <p> 新しいキャプションファイルの場所。 </p> <p>指定しなかった場合、キャプションボタンはユーザーインターフェイスに表示されません。 このパラメーターで指定されたキャプションは、メディアセットの最初のビデオに適用されます。 以降のビデオはキャプションなしで再生されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

1つのメディアセットの参照：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

明示的なメディアセット：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

セット内のすべての画像にシャープ修飾子を追加：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```


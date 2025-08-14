---
title: setAsset
description: 混在メディアビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# setAsset{#setasset}

混在メディアビューア用のJavaScript API リファレンス。

` setAsset( *`asset`*[,data]))`

新しいアセットとオプションの追加アセットデータを設定します。 このパラメーターは、`init()` の前または後であればいつでも呼び出すことができます。 `init()` 後に呼び出された場合、ビューアは実行時にアセットをスワップします。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae) も参照してください。

## パラメーター {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`asset`*` - { `String`} 新しいアセット ID または明示的な混在メディアセット。`?` の後にオプションの画像サービング修飾子が追加されます。

IR （画像レンダリング）または UGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

`*`data`*` – 新しいキャプションファイルの { `JSON`} の場所。

指定しない場合、「キャプション」ボタンはユーザーインターフェイスに表示されません。 このパラメーターで指定されたキャプションは、混在メディアセットの最初のビデオに適用され、後続のビデオはキャプションなしで再生されます。 このビューアは、次のコンポーネント ID をサポートしています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネント ID </p> </th> 
   <th colname="col2" class="entry"> <p>ビューア SDK コンポーネントのクラス名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> postrimage </span> </p> </td> 
   <td colname="col2"> <p>ビデオの再生が開始される前に最初のフレームに表示される画像。 </p> <p>VideoPlayer.posterimage の <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> キュメント </a> 参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> caption </span> </p> </td> 
   <td colname="col2"> <p> 新しいキャプションファイルの場所。 </p> <p>指定しない場合、「キャプション」ボタンはユーザーインターフェイスに表示されません。 このパラメーターで指定されたキャプションは、メディアセットの最初のビデオに適用されます。 後続のビデオはキャプションなしで再生されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

単一メディアセットの参照：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

明示的なメディアセット：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

セット内のすべての画像に追加されたシャープニング修飾子：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```

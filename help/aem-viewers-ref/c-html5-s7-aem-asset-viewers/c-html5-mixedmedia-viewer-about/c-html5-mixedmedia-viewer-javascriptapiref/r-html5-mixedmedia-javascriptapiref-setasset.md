---
title: setAsset
description: 混在メディアビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---

# setAsset{#setasset}

混在メディアビューアの JavaScript API リファレンス。

` setAsset( *`asset`*[,data]))`

新しいアセットとオプションの追加アセットデータを設定します。 このパラメーターは、いつでも（前後に）呼び出すことができます `init()`. 次の後に呼び出された場合 `init()`を指定した場合、ビューアは実行時にアセットをスワップします。

関連トピック [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`アセット`*` - { `String`} 個の新しいアセット ID または明示的な混在メディアセット。オプションの画像サービング修飾子をその後に追加できます。 `?`.

IR（画像レンダリング）または UGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされません。

`*`データ`*` - { `JSON`} 新しいキャプションファイルの場所。

指定しなかった場合、キャプションボタンはユーザーインターフェイスに表示されません。 このパラメーターで指定されたキャプションは、混在メディアセットの最初のビデオに適用されます。後続のビデオはキャプションなしで再生されます。 このビューアでは、次のコンポーネント ID がサポートされています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネント ID </p> </th> 
   <th colname="col2" class="entry"> <p>ビューア SDK のコンポーネントのクラス名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 事後的な </span> </p> </td> 
   <td colname="col2"> <p>ビデオの再生を開始する前の最初のフレームに表示する画像。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> caption </span> </p> </td> 
   <td colname="col2"> <p> 新しいキャプションファイルの場所。 </p> <p>指定しなかった場合、キャプションボタンはユーザーインターフェイスに表示されません。 このパラメーターで指定されたキャプションは、メディアセットの最初のビデオに適用されます。 以降のビデオはキャプションなしで再生されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

単一のメディアセットの参照：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

明示的なメディアセット：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

セット内のすべての画像にシャープ修飾子が追加されました。

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```

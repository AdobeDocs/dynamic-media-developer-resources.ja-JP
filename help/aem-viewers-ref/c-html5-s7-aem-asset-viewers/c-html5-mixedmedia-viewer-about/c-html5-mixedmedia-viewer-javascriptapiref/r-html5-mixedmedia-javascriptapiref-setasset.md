---
title: setAsset
description: Mixed Media ViewerのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
TQID: 'https://experienceleague.adobe.com/Z1AZf1odRYmyN5r7KqKsuOHniQ7inwPAWl-kF7ycItU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 0%

---

# setAsset{#setasset}

Mixed Media ViewerのJavaScript API リファレンス。

` setAsset( *` アセット `*[,data]))`

新しいアセットとオプションの追加アセットデータを設定します。 このパラメーターは、`init()`の前または後に、いつでも呼び出すことができます。 `init()`の後に呼び出された場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae)も参照してください。

## パラメーター {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`asset`*` - { `String`}個の新しいアセット IDまたは明示的な混在メディアセット。オプションの画像サービング修飾子が`?`の後に追加されます。

IR （画像レンダリング）またはUGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

新しいキャプションファイルの`*`data`*` - {`JSON`}の場所。

指定しない場合、キャプションボタンはユーザーインターフェイスに表示されません。 このパラメーターで指定されたキャプションは、混在メディアセットの最初のビデオに適用されます。後続のビデオはキャプションなしで再生されます。 このビューアは、次のコンポーネント IDをサポートしています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネント ID </p> </th> 
   <th colname="col2" class="entry"> <p>Viewer SDK コンポーネントクラス名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">件のポスター画像</span> </p> </td> 
   <td colname="col2"> <p>ビデオの再生を開始する前に、最初のフレームに表示する画像。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> キャプション </span> </p> </td> 
   <td colname="col2"> <p> 新しいキャプションファイルの場所。 </p> <p>指定しない場合、キャプションボタンはユーザーインターフェイスに表示されません。 このパラメーターで指定されたキャプションは、メディアセットの最初のビデオに適用されます。 後続のビデオはキャプションなしで再生されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

単一メディアセット参照：

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

明示的なメディアセット：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

シャープ修飾子がセット内のすべての画像に追加されました。

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```

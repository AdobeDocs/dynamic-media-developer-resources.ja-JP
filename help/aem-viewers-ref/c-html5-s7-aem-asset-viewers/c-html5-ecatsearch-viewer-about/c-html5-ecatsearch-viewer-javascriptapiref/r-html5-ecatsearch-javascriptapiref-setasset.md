---
description: ビデオビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: 5fd80f8d-321e-47f4-9fb2-65e7bd63be58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# setAsset{#setasset}

ビデオビューアのJavaScript APIリファレンス。

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> アセット  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">文字列</span>}新しいアセットIDまたは明示的な画像セット。オプションの画像サービング修飾子を<span class="codeph">の後に付加します。</span>と入力します。 </p> <p> IR（画像レンダリング）またはUGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、[!DNL `init()`]の前後にいつでも呼び出すことができます。 [!DNL `init()`]の後に呼び出した場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

カタログに定義されている画像セットへの1つの参照：

```
 <instance>.setAsset("Viewers/Pluralist")
```

明示的な画像セット（事前に組み合わされたページを含む）:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

明示的な画像セット（個々のページ画像を含む）:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

セット内のすべての画像にシャープ修飾子を追加：

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

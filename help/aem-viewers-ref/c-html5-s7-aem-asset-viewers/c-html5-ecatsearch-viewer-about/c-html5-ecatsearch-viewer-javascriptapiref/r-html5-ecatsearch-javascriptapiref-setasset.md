---
description: ビデオビューア用JavaScript API リファレンス。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5fd80f8d-321e-47f4-9fb2-65e7bd63be58
TQID: 'https://experienceleague.adobe.com/lwSvqbGdXYM1txYvK2of-67envHzyEs4UMsnVmkPKj8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 1%

---

# setAsset{#setasset}

ビデオビューア用JavaScript API リファレンス。

[!DNL ` setAsset( *` アセット `*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> アセット </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>}新しいアセット IDまたはオプションの画像サービング修飾子が<span class="codeph">の後に追加された明示的な画像セット？</span>. </p> <p> IR （画像レンダリング）またはUGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

新しいアセットを設定します。 このパラメーターは、[!DNL `init()`]の前または後に、いつでも呼び出すことができます。 [!DNL `init()`]の後に呼び出された場合、ビューアは実行時にアセットを入れ替えます。

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)も参照してください。

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

カタログで定義されている画像セットへの単一参照：

```
 <instance>.setAsset("Viewers/Pluralist")
```

明示的な画像セット、事前組み合わせページ：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

個々のページ画像を含む明示的な画像セット：

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

シャープ修飾子がセット内のすべての画像に追加されました。

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

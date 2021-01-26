---
description: インラインズームビューアのJavaScript APIリファレンス
seo-description: インラインズームビューアのJavaScript APIリファレンス
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: 75c01024-a734-415a-898a-f91b6bc6a580
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# getComponent{#getcomponent}

インラインズームビューアのJavaScript APIリファレンス

`getComponent(componentId)`

ビューアで使用されているビューアSDKコンポーネントへの参照を返します。 Webページでは、このメソッドを使用して、標準搭載のビューアの動作を拡張またはカスタマイズできます。 このメソッドは、`initComplete`ビューアのコールバックが実行された後にのみ呼び出してください。そうしないと、ビューアのロジックによってコンポーネントがまだ作成されていない場合があります。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`  — ビューア `{String}` が使用するビューアSDKコンポーネントのID。このビューアでは、次のコンポーネントIDがサポートされています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネントID </p> </th> 
   <th colname="col2" class="entry"> <p>ビューアSDKコンポーネントのクラス名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> コンテナ </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.コンテナ  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> flyout  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> swatches  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK APIを使用する場合、[ビューアSDK](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-namespace.md#concept-5af3b472b320496d87735ea612edda80)で説明されているとおり、正しい完全修飾SDK名前空間を使用することが重要です。

特定のコンポーネントについて詳しくは、ビューアSDKのドキュメントを参照してください。

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

`{Object}` ビューアSDKコンポーネントへのリファレンス。`componentId`がサポートされているビューアコンポーネントでない場合、またはビューアのロジックによってコンポーネントがまだ作成されていない場合は、`null`が返されます。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyoutZoomView = <instance>.getComponent("flyout"); 
} 
})
```


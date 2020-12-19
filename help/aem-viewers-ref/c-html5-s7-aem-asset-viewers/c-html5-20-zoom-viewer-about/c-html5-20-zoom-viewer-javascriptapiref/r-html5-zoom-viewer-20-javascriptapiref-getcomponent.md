---
description: ビデオビューアのJavaScript APIリファレンス
seo-description: ビデオビューアのJavaScript APIリファレンス
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: 083e4267-e296-454a-93a1-f0abf24cee94
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 1%

---


# getComponent{#getcomponent}

ビデオビューアのJavaScript APIリファレンス

`getComponent(componentId)`

ビューアで使用されているビューアSDKコンポーネントへの参照を返します。 Webページでは、このメソッドを使用して、標準搭載のビューアの動作を拡張またはカスタマイズできます。 このメソッドは、`initComplete`ビューアのコールバックを実行した後でのみ呼び出してください。呼び出さないと、ビューアのロジックによってコンポーネントがまだ作成されていない場合があります。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`componentID`*`  — ビューア `{String}` が使用するビューアSDKコンポーネントのID。このビューアでは、次のコンポーネントIDがサポートされています。

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
   <td colname="col1"> <p> <span class="codeph"> zoomView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> swatches  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> setIndicator  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SetIndicator  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK APIを使用する場合、[ビューアSDKの名前空間](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-namespace.md#concept-53e47e46d7954e2b9681d13d716fd1ca)で説明されているとおり、正しい完全修飾SDK名前空間を使用することが重要です。

特定のコンポーネントについて詳しくは、ビューアSDK APIドキュメントを参照してください。

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

`{Object}` ビューアSDKコンポーネントへのリファレンス。`componentId`がサポートされているビューアコンポーネントでない場合、またはビューアのロジックによってコンポーネントがまだ作成されていない場合は、`null`が返されます。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```


---
description: カルーセルビューアのJavaScript APIリファレンス。
seo-description: カルーセルビューアのJavaScript APIリファレンス。
seo-title: getComponent**
solution: Experience Manager
title: getComponent**
topic: Dynamic media
uuid: b5449564-c01c-4bb3-b265-b8d70e5f1b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getComponent**{#getcomponent}

カルーセルビューアのJavaScript APIリファレンス。

`getComponent(componentId)`

ビューアで使用されるビューアSDKコンポーネントへの参照を返します。 Webページでは、このメソッドを使用して、標準搭載のビューアの動作を拡張またはカスタマイズできます。 このメソッドは、ビューアのコールバッ `initComplete` クの実行後にのみ呼び出します。呼び出さないと、ビューアのロジックによってコンポーネントがまだ作成されていない可能性があります。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`componentID`*` - `{String}` ビューアで使用されるビューアSDKコンポーネントのID。 このビューアは、次のコンポーネントIDをサポートしています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネントID </p> </th> 
   <th colname="col2" class="entry"> <p>ビューアSDKコンポーネントのクラス名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> コンテナ </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> carouselView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.CarouselView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> controlBar </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> setIndicator </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.SetIndicator </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nextButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> prevButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK APIを使用する場合は、ビューアSDK名前空間で説明されているように、正しい完全修飾SDK名前空間を使 [用することが重要です](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-namespace.md)。

特定のコンポーネントについて詳しくは、ビューアSDK APIドキュメントを参照してください。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアSDKコンポーネントへの参照。 このメソッドは、がサ `null` ポートさ `componentId` れているビューアコンポーネントでない場合、またはビューアのロジックによってコンポーネントがまだ作成されていない場合に返されます。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
} 
})
```


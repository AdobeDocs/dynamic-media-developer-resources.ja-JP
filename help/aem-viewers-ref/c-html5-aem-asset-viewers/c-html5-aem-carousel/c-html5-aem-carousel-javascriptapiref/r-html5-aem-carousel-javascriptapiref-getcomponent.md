---
title: getComponent
description: カルーセルビューアのJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 088d99d0-600d-4e47-85ea-a9769938b88b
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# getComponent {#getcomponent}

カルーセルビューアのJavaScript API リファレンス。

`getComponent(componentId)`

ビューアによって使用されるビューアSDKコンポーネントへの参照を返します。 Web ページでは、この方法を使用して、標準ビューアの動作を拡張またはカスタマイズできます。 このメソッドは `initComplete` ビューアコールバックが実行された後にのみ呼び出します。それ以外の場合、コンポーネントはビューアロジックによってまだ作成されていない可能性があります。

## パラメーター {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - ビューアが使用するビューア SDK コンポーネントの ID を `{String}` します。 このビューアは、次のコンポーネント ID をサポートしています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネント ID </p> </th> 
   <th colname="col2" class="entry"> <p>ビューア SDK コンポーネントのクラス名 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> controlBar </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> setIndicator</span> </p> </td> 
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

SDK API を使用する場合は、[&#x200B; ビューア SDK名前空間 &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-namespace.md) に記載されているように、正しい完全修飾SDK名前空間を使用することが重要です。

特定のコンポーネントについて詳しくは、ビューアのSDK API ドキュメントを参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアのSDK コンポーネントへの参照。 `null` がサポートされているビューアコンポーネントでない場合や、コンポーネントがまだビューアロジックで作成されていない場合、メソッドは `componentId` を返します。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
} 
})
```

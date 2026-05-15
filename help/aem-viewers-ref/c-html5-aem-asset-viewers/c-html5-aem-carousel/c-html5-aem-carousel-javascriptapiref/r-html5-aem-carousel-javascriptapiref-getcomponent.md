---
title: getComponent
description: カルーセルビューア用JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 088d99d0-600d-4e47-85ea-a9769938b88b
TQID: 'https://experienceleague.adobe.com/Ijo9j5-s9WpsFIeFhFdAwp2cHaQfOFZ-OYM67qe3T3g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 181
ht-degree: 0%

---

# getComponent {#getcomponent}

カルーセルビューア用JavaScript API リファレンス。

`getComponent(componentId)`

ビューアで使用されるビューア SDK コンポーネントへの参照を返します。 Web ページでは、このメソッドを使用して、標準ビューアの動作を拡張またはカスタマイズできます。 このメソッドは、`initComplete` ビューア コールバックが実行された後にのみ呼び出します。そうしないと、ビューア ロジックによってまだコンポーネントが作成されない可能性があります。

## パラメーター {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}`は、ビューアで使用されるビューア SDK コンポーネントのIDです。 このビューアは、次のコンポーネント IDをサポートしています。

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コンポーネント ID </p> </th> 
   <th colname="col2" class="entry"> <p>Viewer SDK コンポーネントクラス名 </p> </th> 
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
   <td colname="col1"> <p> <span class="codeph"> カルーセルビュー</span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph">前ボタン </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK APIを使用する場合は、[Viewer SDK名前空間](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-namespace.md)で説明されているように、正しい完全修飾SDK名前空間を使用することが重要です。

特定のコンポーネントについて詳しくは、Viewer SDK API ドキュメントを参照してください。

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Viewer SDK コンポーネントへの参照。 このメソッドは、`componentId`がサポートされているビューアコンポーネントでない場合、またはビューアロジックによってコンポーネントがまだ作成されていない場合、`null`を返します。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
} 
})
```

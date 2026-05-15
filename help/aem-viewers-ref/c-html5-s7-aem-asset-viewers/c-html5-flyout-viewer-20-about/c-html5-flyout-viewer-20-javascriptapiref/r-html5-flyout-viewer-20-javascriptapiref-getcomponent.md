---
title: getComponent
description: Flyout Viewer用JavaScript API リファレンス
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 618d34af-32d0-45bd-928d-7a4e084edbe6
TQID: 'https://experienceleague.adobe.com/zNEf4My7yXhnvzacB4w0ReB0Ytb000AI4g8AH-dx7vI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 0%

---

# getComponent{#getcomponent}

Flyout Viewer用JavaScript API リファレンス

`getComponent(componentId)`

ビューアで使用されるビューア SDK コンポーネントへの参照を返します。 Web ページでは、このメソッドを使用して、標準ビューアの動作を拡張またはカスタマイズできます。 このメソッドは、`initComplete` ビューア コールバックが実行された後にのみ呼び出します。そうでない場合、ビューア ロジックによってまだコンポーネントが作成されない可能性があります。

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
   <td colname="col1"> <p> <span class="codeph"> フライアウト </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">個のスウォッチ </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK APIを使用する場合は、[Viewer SDK](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-namespace.md#concept-453501a601634dd1bca7b96878c22605)で説明されているように、正しい完全修飾SDK名前空間を使用することが重要です。

特定のコンポーネントについて詳しくは、Viewer SDK API ドキュメントを参照してください。

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Viewer SDK コンポーネントへの参照。 このメソッドは、`componentId`がサポートされているビューアコンポーネントでない場合、またはビューアロジックによってコンポーネントがまだ作成されていない場合、`null`を返します。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyoutZoomView = <instance>.getComponent("flyout"); 
} 
})
```

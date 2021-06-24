---
description: 基本ズームビューアのJavaScript APIリファレンス
solution: Experience Manager
title: getComponent
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,Business Practitioner
exl-id: e9bf641f-5bc9-42d9-a030-5591cd883373
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---

# getComponent{#getcomponent}

基本ズームビューアのJavaScript APIリファレンス

`getComponent(componentId)`

ビューアで使用されるビューアSDKコンポーネントへの参照を返します。 Webページでは、この方法を使用して、標準提供ビューアの動作を拡張またはカスタマイズできます。 このメソッドは、`initComplete`ビューアのコールバックを実行した後にのみ呼び出します。そうしないと、ビューアのロジックによってコンポーネントがまだ作成されていない可能性があります。

## パラメータ {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`  - `{String}` ビューアで使用されるビューアSDKコンポーネントのID。このビューアは、次のコンポーネントIDをサポートしています。

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
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container  </span> </p> </td> 
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

SDK APIを操作する場合は、ビューアSDKの名前空間で説明されているように、正しい完全修飾SDK名前空間を使用することが重要です

特定のコンポーネントについて詳しくは、ビューアSDK APIのドキュメントを参照してください。

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` ビューアSDKコンポーネントへのリファレンス。`componentId`がサポートされているビューアコンポーネントでない場合、またはビューアのロジックによってコンポーネントがまだ作成されていない場合、メソッドは`null`を返します。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```

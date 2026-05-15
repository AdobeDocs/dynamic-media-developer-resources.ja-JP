---
title: getComponent
description: パノラマビューアのJavaScript API リファレンス。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
autotag-review: '2026-05-13T22:09:12.361Z'
TQID: 'https://experienceleague.adobe.com/6tWQNhwyzc-PV8TLegYBXSzAYEMkVKyvGCu5BDv2uIo'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# getComponent{#getcomponent}

パノラマビューア用JavaScript API リファレンス

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
   <td colname="col1"> <p> <span class="codeph"> パノラマビュー</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.PanoramicView </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

SDK APIを使用する場合は、[Viewer SDK名前空間](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621)で説明されているように、正しい完全修飾SDK名前空間を使用することが重要です。

特定のコンポーネントについて詳しくは、Viewer SDK API ドキュメントを参照してください。

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`は、Viewer SDK コンポーネントへの参照です。 このメソッドは、`componentId`がサポートされているビューアコンポーネントでない場合、またはビューアロジックによってコンポーネントがまだ作成されていない場合、`null`を返します。

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
} 
})
```

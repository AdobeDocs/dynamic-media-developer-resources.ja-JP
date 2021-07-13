---
description: eCatalogビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: 33779874-2ab9-490a-8eaf-726adaa76327
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# setHandlers{#sethandlers}

eCatalogビューアのJavaScript APIリファレンス。

[!DNL `setHandlers(handlers)`]

0個以上のコールバックハンドラーを指定します。 このメソッドを呼び出すと、そのビューアインスタンスに以前に割り当てられたイベントハンドラーが完全に上書きされます。 `init()`の前に呼び出す必要があります。

## パラメータ {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handlers  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}ビュー </span> アのイベントコールバックを含むJSONオブジェクト。プロパティ名はサポートされているビューアイベントの名前、プロパティ値は適切なコールバックに対するJavaScript関数参照です。 </p> <p>ビューアイベントについて詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local">イベントコールバック</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

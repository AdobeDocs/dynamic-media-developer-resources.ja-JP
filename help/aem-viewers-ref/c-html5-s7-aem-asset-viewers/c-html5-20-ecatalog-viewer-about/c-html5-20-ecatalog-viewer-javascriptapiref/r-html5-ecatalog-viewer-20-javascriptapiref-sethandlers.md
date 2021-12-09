---
title: setHandlers
description: eCatalog ビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: a6709da7-1fa2-421b-8c99-a4ccea83c600
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 3%

---

# setHandlers{#sethandlers}

eCatalog ビューアの JavaScript API リファレンス。

`setHandlers(handlers)`

0 個以上のコールバックハンドラを指定します。 このメソッドを呼び出すと、そのビューアインスタンスに対して以前に割り当てられていたイベントハンドラーが完全に上書きされます。 の前に呼び出す必要があります `init()`.

## パラメータ {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ハンドラー </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> ビューアのイベントコールバックを含む JSON オブジェクト。プロパティ名はサポートされているビューアイベントの名前、プロパティ値は適切なコールバックへの JavaScript 関数参照です。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> イベントコールバック </a> を参照してください。 </p> </td> 
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

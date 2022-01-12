---
title: setHandlers
description: インラインズームビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 233fadf5-4b09-406d-959b-c2c9c4524021
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# setHandlers{#sethandlers}

インラインズームビューアの JavaScript API リファレンス。

`setHandlers(handlers)`

0 個以上のコールバックハンドラを指定します。 このメソッドを呼び出すと、そのビューアインスタンスに対して以前に割り当てられていたイベントハンドラーが完全に上書きされます。 の前に呼び出す必要があります `init()`.

## パラメータ {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ハンドラー </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> ビューアのイベントコールバックを含む JSON オブジェクト。プロパティ名はサポートされているビューアイベントの名前、プロパティ値は適切なコールバックへの JavaScript 関数参照です。 </p> <p>詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> イベントコールバック </a> を参照してください。 </p> </td> 
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

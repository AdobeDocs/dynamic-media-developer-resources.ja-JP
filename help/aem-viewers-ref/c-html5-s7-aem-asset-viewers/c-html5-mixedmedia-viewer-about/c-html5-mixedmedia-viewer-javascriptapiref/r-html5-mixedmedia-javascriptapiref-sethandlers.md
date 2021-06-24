---
description: 混在メディアビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: e30f1b73-1dba-4d4c-9e90-f343ca404550
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# setHandlers{#sethandlers}

混在メディアビューアのJavaScript APIリファレンス。

`setHandlers(handlers)`

0個以上のコールバックハンドラーを指定します。 このメソッドを呼び出すと、そのビューアインスタンスに以前に割り当てられたイベントハンドラーが完全に上書きされます。 `init()`の前に呼び出す必要があります。

## パラメータ {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handlers  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}ビュー </span> アのイベントコールバックを含むJSONオブジェクト。プロパティ名はサポートされているビューアイベントの名前、プロパティ値は適切なコールバックに対するJavaScript関数参照です。 </p> <p>ビューアイベントについて詳しくは、 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local">イベントコールバック</a>を参照してください。 </p> </td> 
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

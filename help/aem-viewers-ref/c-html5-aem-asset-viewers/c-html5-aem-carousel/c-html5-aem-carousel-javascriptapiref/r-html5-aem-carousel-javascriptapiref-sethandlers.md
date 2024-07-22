---
title: setHandlers
description: カルーセルビューアのJavaScript API リファレンス
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d269627a-e2f8-4ca6-96a1-a7dce312e06e
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# setHandlers{#sethandlers}

カルーセルビューアのJavaScript API リファレンス

`setHandlers(handlers)`

0 個以上のコールバックハンドラーを指定します。 このメソッドを呼び出すと、そのビューアインスタンスに以前に割り当てられていたイベントハンドラーが完全に上書きされます。 `init()` 前に呼び出す必要があります。

## パラメータ {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handlers </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} ビューアイベント </span> コールバックを持つ JSON オブジェクト。 プロパティ名は、サポートされているビューアイベントの名前です。 このプロパティ値は、適切なコールバックへのJavaScript関数の参照です。 </p> <p>ビューアイベントについて詳しくは、<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Event callbacks </a> を参照してください。 </p> </td> 
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

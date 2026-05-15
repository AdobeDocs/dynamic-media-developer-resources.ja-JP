---
title: setHandlers
description: カルーセルビューア用JavaScript API リファレンス
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d269627a-e2f8-4ca6-96a1-a7dce312e06e
TQID: 'https://experienceleague.adobe.com/E9gW0XQoGv26n0Mt4H-BqZ0Fw41cG1OgaAbV6lslfIg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 3%

---

# setHandlers{#sethandlers}

カルーセルビューア用JavaScript API リファレンス

`setHandlers(handlers)`

0個以上のコールバックハンドラーを指定します。 このメソッドの呼び出しは、以前にそのビューアーインスタンスに割り当てられたイベントハンドラーを完全に上書きします。 `init()`の前に呼び出す必要があります。

## パラメータ {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ハンドラー</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> ビューア イベント コールバックを含むJSON オブジェクト。 プロパティ名は、サポートされているビューアイベントの名前です。 プロパティ値は、適切なコールバックへのJavaScript関数参照です。 </p> <p>ビューアイベントの詳細については、<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> イベントコールバック </a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

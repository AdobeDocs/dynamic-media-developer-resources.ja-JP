---
description: カルーセルビューアのJavaScript APIリファレンス
seo-description: カルーセルビューアのJavaScript APIリファレンス
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 5e1e9c8f-866b-4730-9978-b45face85667
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setHandlers{#sethandlers}

カルーセルビューアのJavaScript APIリファレンス

`setHandlers(handlers)`

0個以上のコールバックハンドラーを指定します。 このメソッドを呼び出すと、そのビューアインスタンスに以前に割り当てられたイベントハンドラーが完全に上書きされます。 前に呼び出す必要がありま `init()`す。

## パラメータ {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ハンドラ <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}ビューアのイベ </span> ントコールバックを含むJSONオブジェクト。 プロパティ名は、サポートされているビューアイベントの名前です。 プロパティ値は、適切なコールバックへのJavaScript関数参照です。 </p> <p>ビューアイベ <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> ントについて詳し </a> くは、イベントコールバックを参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```


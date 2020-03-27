---
description: スピンビューアのJavaScript APIリファレンス
seo-description: スピンビューアのJavaScript APIリファレンス
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 50db47ee-c1bb-4e45-bfcf-fae0fff6e0e8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setHandlers{#sethandlers}

スピンビューアのJavaScript APIリファレンス

`setHandlers(handlers)`

0個以上のコールバックハンドラーを指定します。 このメソッドを呼び出すと、そのビューアインスタンスに以前に割り当てられたイベントハンドラーが完全に上書きされます。 前に呼び出す必要がありま `init()`す。

## パラメータ {#section-51f820ded5e842bebd123e37a35176c7}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ハンドラ <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}ビューアのイベントコールバックを含む </span> JSONオブジェクト。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックへのJavaScript関数参照です。 </p> <p>ビューアイベ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> ントについて詳し </a> くは、イベントコールバックを参照してください。 </p> </td> 
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


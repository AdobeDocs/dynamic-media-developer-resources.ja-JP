---
description: ビデオビューアのJavaScript APIリファレンス
seo-description: ビデオビューアのJavaScript APIリファレンス
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: d69160bf-b4de-4cde-8173-bf4da601a265
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---


# setHandlers{#sethandlers}

ビデオビューアのJavaScript APIリファレンス

`setHandlers(handlers)`

0個以上のコールバックハンドラーを指定します。 このメソッドを呼び出すと、そのビューアインスタンスに以前割り当てられたイベントハンドラーが完全に上書きされます。 `init()`の前に呼び出す必要があります。

## パラメータ {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handlers  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}ビューアのイベントコールバックを含む </span> JSONオブジェクト。プロパティ名はサポートされているビューアイベントの名前で、プロパティ値は適切なコールバックに対するJavaScript関数参照です。 </p> <p>ビューアのイベントについて詳しくは、<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local">イベントコールバック</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```


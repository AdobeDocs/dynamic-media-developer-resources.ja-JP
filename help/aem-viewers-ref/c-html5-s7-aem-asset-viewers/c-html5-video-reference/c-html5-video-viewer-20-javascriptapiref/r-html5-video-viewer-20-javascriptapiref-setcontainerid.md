---
description: ビデオビューアのJavaScript APIリファレンス。
seo-description: ビデオビューアのJavaScript APIリファレンス。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic Media
uuid: a4b741a1-b0b3-4bc3-aeab-9d0e44ec4e79
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---


# setContainerId{#setcontainerid}

ビデオビューアのJavaScript APIリファレンス。

` setContainerId( *`containerId`*)`

ビューアの挿入先のDOMコンテナ（通常は`DIV`）のIDを設定します。 このメソッドを呼び出すまでにコンテナ要素を作成しておく必要はありません。 ただし、`init()`を実行する際にはコンテナが存在している必要があります。 このパラメーターは`init()`の前に呼び出されます。 ビューアの設定情報が`config` JSONオブジェクトを使用して渡される場合は、このメソッドはオプションです。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}コンテナの </span> ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101}を返す

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```


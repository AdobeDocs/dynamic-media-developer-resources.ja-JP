---
description: カルーセルビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic，ビューア，SDK/API，カルーセルバナー
role: Developer,Business Practitioner
exl-id: 32636cf9-3dc7-4299-a7b7-cf803ca36514
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

カルーセルビューアのJavaScript APIリファレンス。

` setContainerId( *`containerId`*)`

ビューアを挿入するDOMコンテナ（通常は`DIV`）のIDを設定します。 このメソッドを呼び出すまでにコンテナ要素を作成する必要はありません。 ただし、`init()`を実行する際にはコンテナが存在する必要があります。 `init()`の前に呼び出す必要があります。

ビューアの設定情報が`config` JSONオブジェクトを使用して渡される場合は、このメソッドはオプションです。

## パラメータ {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}コン </span> テナのID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

---
description: ビデオ画像ビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setContainerId
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブ画像
role: 開発者、業務従事者
exl-id: 2b9b89e6-50ea-458f-9da2-6fda1884935c
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

ビデオ画像ビューアのJavaScript APIリファレンス。

` setContainerId( *`containerId`*)`

ビューアを挿入するDOMコンテナ（通常はDIV）のIDを設定します。 このメソッドを呼び出すまでにコンテナ要素を作成しておく必要はありません。 ただし、`init()`を実行する際にはコンテナが存在している必要があります。 `init()`の前に呼び出す必要があります。

ビューアの設定情報が`config` JSONオブジェクトを使用して渡される場合は、このメソッドはオプションです。

## パラメータ {#section-fa807db629ce43bab286b1e1dc96c492}

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

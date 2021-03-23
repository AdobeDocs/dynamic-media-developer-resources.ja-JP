---
description: eCatalogビューアのJavaScript APIリファレンス。
seo-description: eCatalogビューアのJavaScript APIリファレンス。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
uuid: 9aed8cb6-d89b-41f6-bd87-e390bb6002a5
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# setContainerId{#setcontainerid}

eCatalogビューアのJavaScript APIリファレンス。

` setContainerId( *`containerId`*)`

ビューアを挿入する`DOM`コンテナ（通常は`DIV`）のIDを設定します。 このメソッドを呼び出すまでにコンテナ要素を作成しておく必要はありません。 ただし、`init()`を実行する際にはコンテナが存在している必要があります。 `init()`の前に呼び出す必要があります。

ビューアの設定情報が`config` JSONオブジェクトを使用して渡される場合は、このメソッドはオプションです。

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


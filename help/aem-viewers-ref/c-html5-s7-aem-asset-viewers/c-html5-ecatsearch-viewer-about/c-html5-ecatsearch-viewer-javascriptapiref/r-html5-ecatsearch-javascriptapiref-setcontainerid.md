---
description: eCatalogビューアのJavaScript APIリファレンス。
seo-description: eCatalogビューアのJavaScript APIリファレンス。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 19149e38-b9d2-4ecd-a555-92e2960f7ee3
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setContainerId{#setcontainerid}

eCatalogビューアのJavaScript APIリファレンス。

[!DNL ` setContainerId( *`containerId`*)`]

ビューアを挿入する[!DNL `DOM` コンテナ(通常はa [!DNL `DIV`])のIDを設定します。 このメソッドを呼び出すまでにコンテナ要素を作成しておく必要はありません。 ただし、を実行する際にはコンテナが存在する必 [!DNL `init()`] 要があります。 前に呼び出す必要がありま [!DNL `init()`]す。

ビューアの設定情報が [!DNL `config`] JSONオブジェクトと共にコンストラクターに渡される場合、このメソッドはオプションです。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}コン </span> テナのID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```


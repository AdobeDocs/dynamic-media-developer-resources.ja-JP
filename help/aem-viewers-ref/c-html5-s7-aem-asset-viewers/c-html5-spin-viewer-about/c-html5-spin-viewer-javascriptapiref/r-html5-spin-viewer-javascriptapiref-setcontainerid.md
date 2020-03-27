---
description: スピンビューアのJavaScript APIリファレンス。
seo-description: スピンビューアのJavaScript APIリファレンス。
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 6ed57f8f-5a5e-4dfa-9ab5-0f724603a0bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setContainerId{#setcontainerid}

スピンビューアのJavaScript APIリファレンス。

` setContainerId( *`containerId`*)`

ビューアを挿入するDOMコンテナ（通常はDIV）のIDを設定します。 このメソッドを呼び出すまでにコンテナ要素を作成しておく必要はありません。 ただし、を実行する際にはコンテナが存在する必 `init()` 要があります。 前に呼び出す必要がありま `init()`す。

ビューアの設定情報が `config` JSONオブジェクトと共にコンストラクターに渡される場合、このメソッドはオプションです。

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


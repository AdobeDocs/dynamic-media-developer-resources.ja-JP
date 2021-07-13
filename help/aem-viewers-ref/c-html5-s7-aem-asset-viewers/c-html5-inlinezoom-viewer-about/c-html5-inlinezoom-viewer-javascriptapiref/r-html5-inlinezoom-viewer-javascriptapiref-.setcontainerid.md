---
description: インラインズームビューアのJavaScript APIリファレンス。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,User
exl-id: ab3359f0-0c58-4984-815a-e0246728100e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

インラインズームビューアのJavaScript APIリファレンス。

` setContainerId( *`containerId`*)`

ビューアを挿入するDOMコンテナ（通常は`DIV`）のIDを設定します。 このメソッドを呼び出すまでにコンテナ要素を作成する必要はありません。 ただし、`init()`を実行する際にはコンテナが存在する必要があります。 `init()`の前に呼び出す必要があります。 ビューアの設定情報が`config` JSONオブジェクトを使用してコンストラクターに渡される場合は、このメソッドはオプションです。

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

---
title: setContainerId
description: ビデオビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 9f2857a4-108d-4689-9c39-cb2635405d0d
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

ビデオビューア用のJavaScript API リファレンス。

` setContainerId( *`containerId`*)`

ビューアを挿入する DOM コンテナの ID （通常は `DIV`）を設定します。 このメソッドが呼び出されるまでにコンテナ要素を作成する必要はありません。 ただし、`init()` を実行する場合は、コンテナが存在している必要があります。 このパラメーターは、`init()` 前に呼び出されます。 ビューアの設定情報が JSON オブジェクトとともにコンストラクターに渡され `config` 場合、このメソッドはオプションです。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} コンテナ </span>ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

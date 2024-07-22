---
title: setContainerId
description: スマート切り抜きビデオビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 1c7a7494-e872-4e78-9518-ea30af46303c
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

スマート切り抜きビデオビューア用のJavaScript API リファレンス。

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

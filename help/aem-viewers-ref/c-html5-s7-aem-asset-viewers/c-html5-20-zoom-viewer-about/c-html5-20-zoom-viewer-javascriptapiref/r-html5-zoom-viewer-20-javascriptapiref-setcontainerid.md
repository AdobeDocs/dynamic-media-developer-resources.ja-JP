---
title: setContainerId
description: ビデオビューア用JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 87f01c5f-0d2a-46d6-8026-e75e879532df
TQID: 'https://experienceleague.adobe.com/nC5uMmUTFpcnJtX3-Piu6uQvOo69guTD4maneYk0rTw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 2%

---

# setContainerId{#setcontainerid}

ビデオビューア用JavaScript API リファレンス。

` setContainerId( *`containerId`*)`

ビューアが挿入されるDOM コンテナ（通常はDIV）のIDを設定します。 このメソッドが呼び出されるまでにコンテナ要素を作成する必要はありません。 ただし、`init()`の実行時には、コンテナが存在する必要があります。 `init()`の前に呼び出す必要があります。

ビューア設定情報が`config` JSON オブジェクトでコンストラクターに渡された場合、このメソッドはオプションです。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> コンテナ ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

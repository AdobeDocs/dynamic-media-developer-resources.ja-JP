---
title: setContainerId
description: ビデオビューア用のJavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 87f01c5f-0d2a-46d6-8026-e75e879532df
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

ビデオビューア用のJavaScript API リファレンス。

` setContainerId( *`containerId`*)`

ビューアが挿入される DOM コンテナの ID （通常は DIV）を設定します。 このメソッドが呼び出されるまでにコンテナ要素を作成する必要はありません。 ただし、`init()` を実行する場合は、コンテナが存在している必要があります。 `init()` る前に呼び出す必要があります。

ビューア設定情報が JSON オブジェクトとともにコンストラクターに渡された場合 `config` このメソッドはオプションです。

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

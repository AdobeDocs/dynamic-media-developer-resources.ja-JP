---
title: setContainerId
description: ビデオビューアの JavaScript API リファレンス。
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

ビデオビューアの JavaScript API リファレンス。

` setContainerId( *`containerId`*)`

ビューアを挿入する DOM コンテナ（通常は DIV）の ID を設定します。 このメソッドを呼び出すまでにコンテナ要素を作成する必要はありません。 ただし、コンテナは、 `init()` が実行されます。 の前に呼び出す必要があります。 `init()`.

ビューアの設定情報がで渡された場合は、このメソッドはオプションです。 `config` JSON オブジェクトをコンストラクターに渡します。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> コンテナの ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

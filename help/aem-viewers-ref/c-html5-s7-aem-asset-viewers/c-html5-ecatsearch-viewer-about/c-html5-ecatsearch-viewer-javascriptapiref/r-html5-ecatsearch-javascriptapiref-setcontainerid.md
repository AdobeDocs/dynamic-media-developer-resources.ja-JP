---
description: eCatalog ビューアのJavaScript API リファレンス。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f1491091-f109-4836-b7f1-ad0619b72dce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

eCatalog ビューアのJavaScript API リファレンス。

[!DNL ` setContainerId( *`containerId`*)`]

ビューアが挿入される `DOM` コンテナの ID （通常は `DIV`）を設定します。 このメソッドが呼び出されるまでにコンテナ要素を作成する必要はありません。 ただし、`init()` を実行する場合は、コンテナが存在している必要があります。 `init()` る前に呼び出す必要があります。

ビューアの設定情報が JSON オブジェクトとともにコンストラクターに渡され `config` 場合、このメソッドはオプションです。

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

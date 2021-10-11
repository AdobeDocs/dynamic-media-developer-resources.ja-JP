---
title: setContainerId
description: Video360 ビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b0145fb0-2b0d-40ce-ac18-029f54bc4050
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

Video360 ビューアの JavaScript API リファレンス。

` setContainerId( *`containerId`*)`

ビューアを挿入する DOM コンテナ（通常は DIV）の ID を設定します。 このメソッドを呼び出すまでにコンテナ要素を作成しておく必要はありません。 ただし、`init()` を実行する際には、コンテナが存在する必要があります。 `init()` の前に呼び出す必要があります。

ビューアの設定情報が `config` JSON オブジェクトを使用して渡される場合は、このメソッドはオプションです。

## パラメータ {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} コンテ </span> ナの ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

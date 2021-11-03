---
description: スマート切り抜きビデオビューアの JavaScript API リファレンス。
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 9f2857a4-108d-4689-9c39-cb2635405d0d
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

スマート切り抜きビデオビューアの JavaScript API リファレンス。

` setContainerId( *`containerId`*)`

DOM コンテナの ID を設定します ( 通常は `DIV`) をクリックします。 このメソッドを呼び出すまでにコンテナ要素を作成する必要はありません。 ただし、コンテナは、 `init()` が実行されます。 このパラメーターは、 `init()`. ビューアの設定情報が `config` JSON オブジェクトをコンストラクターに追加します。

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

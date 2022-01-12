---
title: setContainerId
description: フライアウトビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 5e07cbba-c1c1-4c85-af2b-ab2d84fbb709
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

フライアウトビューアの JavaScript API リファレンス。

` setContainerId( *`containerId`*)`

DOM コンテナの ID を設定します ( 通常は `DIV`) を使用して、ビューアを挿入します。 このメソッドを呼び出すまでにコンテナ要素を作成する必要はありません。 ただし、コンテナは、 `init()` が実行されます。 の前に呼び出す必要があります。 `init()`. ビューアの設定情報が `config` JSON オブジェクトをコンストラクターに追加します。

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

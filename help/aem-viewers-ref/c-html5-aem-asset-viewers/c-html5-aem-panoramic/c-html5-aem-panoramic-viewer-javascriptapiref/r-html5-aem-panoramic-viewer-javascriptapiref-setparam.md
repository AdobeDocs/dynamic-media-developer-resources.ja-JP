---
title: setParam
description: パノラマビューアのJavaScript API リファレンス。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
autotag-review: '2026-05-13T22:11:37.806Z'
TQID: 'https://experienceleague.adobe.com/Hw4SgeJ8yTvGg1zDyDkqtWH6gfGdIHa0daPZ7cT6eow'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 2%

---

# setParam{#setparam}

パノラマビューアのJavaScript API リファレンス。

` setParam( *`name, value`*)`

ビューアパラメーターを指定した値に設定します。 パラメーターは、ビューア固有の設定オプションまたはソフトウェア開発キット修飾子です。 このパラメーターは`init()`の前に呼び出されます。

ビューア設定情報が`config` JSON オブジェクトでコンストラクターに渡された場合、このメソッドはオプションです。



<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">名</span> </span> </p> </td> 
   <td colname="col2"> <p> パラメーターの<span class="codeph"> {string} </span>名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">値</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> パラメーターの値。 値をパーセント エンコードすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```

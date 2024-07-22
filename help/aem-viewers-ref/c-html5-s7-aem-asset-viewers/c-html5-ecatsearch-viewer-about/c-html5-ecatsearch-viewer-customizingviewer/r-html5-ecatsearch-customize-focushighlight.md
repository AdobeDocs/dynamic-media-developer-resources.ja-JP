---
title: フォーカスのハイライト
description: フォーカスされたビューアのユーザーインターフェイス要素の周囲に表示された入力フォーカスハイライト。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# フォーカスのハイライト{#focus-highlight}

フォーカスされたビューアのユーザーインターフェイス要素の周囲に表示された入力フォーカスハイライト。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

フォーカスハイライトの外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogviewer *:focus
```

**フォーカスハイライト表示の CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 概要 </span> </p> </td> 
   <td colname="col2"> <p> フォーカスハイライトのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – すべてのビューアのユーザーインターフェイス要素に対してデフォルトのブラウザーフォーカスハイライトを無効にするには、ビューアのスタイルシートに次の CSS セレクターを追加します。

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

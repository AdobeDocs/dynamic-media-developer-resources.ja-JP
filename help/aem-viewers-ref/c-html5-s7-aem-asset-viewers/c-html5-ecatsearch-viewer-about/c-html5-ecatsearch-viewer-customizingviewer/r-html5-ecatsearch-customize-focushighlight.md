---
title: フォーカスのハイライト
description: フォーカスされたビューアのユーザインターフェイス要素の周囲に表示される入力フォーカスのハイライト。
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

フォーカスされたビューアのユーザインターフェイス要素の周囲に表示される入力フォーカスのハイライト。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

フォーカスハイライトの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer *:focus
```

**フォーカスハイライトの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 概要 </span> </p> </td> 
   <td colname="col2"> <p> フォーカスのハイライトのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — すべてのビューアユーザインターフェイス要素の初期設定のブラウザフォーカスハイライトを無効にするには、ビューアのスタイルシートに次の CSS セレクターを追加します。

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

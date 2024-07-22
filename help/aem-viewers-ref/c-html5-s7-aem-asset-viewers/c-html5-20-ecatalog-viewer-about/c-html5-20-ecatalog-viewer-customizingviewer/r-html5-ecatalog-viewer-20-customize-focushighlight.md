---
title: フォーカスのハイライト
description: フォーカスされたビューアのユーザーインターフェイス要素の周囲に表示された入力フォーカスハイライト。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
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

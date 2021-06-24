---
description: フォーカスされたビューアのユーザインターフェイス要素の周囲に表示される入力フォーカスのハイライト。
solution: Experience Manager
title: フォーカスハイライト
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,Business Practitioner
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# フォーカスハイライト{#focus-highlight}

フォーカスされたビューアのユーザインターフェイス要素の周囲に表示される入力フォーカスのハイライト。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

フォーカスハイライトの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer *:focus
```

**フォーカスハイライトのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> アウトライン  </span> </p> </td> 
   <td colname="col2"> <p> フォーカスハイライトのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — すべてのビューアユーザインターフェイス要素の初期設定のブラウザフォーカスハイライトを無効にするには、ビューアのスタイルシートに次のCSSセレクタを追加します。

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

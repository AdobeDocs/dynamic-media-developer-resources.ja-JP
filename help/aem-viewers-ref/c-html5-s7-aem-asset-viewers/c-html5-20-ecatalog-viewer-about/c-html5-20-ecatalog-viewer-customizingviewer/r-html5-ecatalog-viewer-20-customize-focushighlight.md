---
description: フォーカスが設定されたビューアのユーザインターフェイス要素の周りに表示される入力フォーカスハイライト。
seo-description: フォーカスが設定されたビューアのユーザインターフェイス要素の周りに表示される入力フォーカスハイライト。
seo-title: フォーカスハイライト
solution: Experience Manager
title: フォーカスハイライト
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---


# フォーカスハイライト{#focus-highlight}

フォーカスが設定されたビューアのユーザインターフェイス要素の周りに表示される入力フォーカスハイライト。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

フォーカスハイライトの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer *:focus
```

**フォーカスハイライトのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> outline  </span> </p> </td> 
   <td colname="col2"> <p> フォーカスのハイライトのスタイル </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — すべてのビューアユーザインターフェイス要素の初期設定のブラウザフォーカスハイライトを無効にするには、以下のCSSセレクターをビューアのスタイルシートに追加します。

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```


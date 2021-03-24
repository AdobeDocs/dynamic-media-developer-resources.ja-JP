---
description: フォーカスが設定されたビューアのユーザインターフェイス要素の周りに表示される入力フォーカスハイライト。
solution: Experience Manager
title: フォーカスハイライト
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
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


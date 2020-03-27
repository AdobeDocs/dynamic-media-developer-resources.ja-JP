---
description: フォーカスされたビューアのユーザインターフェイス要素の周囲に表示される入力フォーカスハイライト。
seo-description: フォーカスされたビューアのユーザインターフェイス要素の周囲に表示される入力フォーカスハイライト。
seo-title: フォーカスハイライト
solution: Experience Manager
title: フォーカスハイライト
topic: Dynamic media
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# フォーカスハイライト{#focus-highlight}

フォーカスされたビューアのユーザインターフェイス要素の周囲に表示される入力フォーカスハイライト。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

フォーカスハイライトの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer *:focus
```

**フォーカスハイライトのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 輪郭 </span> </p> </td> 
   <td colname="col2"> <p> フォーカスのハイライトのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — ビューアのすべてのユーザインターフェイス要素の初期設定のブラウザフォーカスハイライトを無効にするには、次のCSSセレクターをビューアのスタイルシートに追加します。

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```


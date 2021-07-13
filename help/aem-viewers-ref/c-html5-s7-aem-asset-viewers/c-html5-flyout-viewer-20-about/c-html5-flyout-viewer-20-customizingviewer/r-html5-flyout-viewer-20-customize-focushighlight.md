---
description: フォーカスされたビューアのUI要素の周囲に表示される入力フォーカスのハイライトは、CSSクラスセレクターを使用して制御します。
solution: Experience Manager
title: フォーカスハイライト
feature: Dynamic Media Classic，ビューア，SDK/API，フライアウト
role: Developer,User
exl-id: 2cb2e719-ee56-45e5-a509-7e13bb3c2165
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 1%

---

# フォーカスハイライト{#focus-highlight}

フォーカスされたビューアのUI要素の周囲に表示される入力フォーカスのハイライトは、CSSクラスセレクターを使用して制御します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSSプロパティ**

外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7flyoutviewer *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> アウトライン  </span> </p> </td> 
   <td colname="col2"> <p>フォーカスハイライトのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — すべてのビューアユーザインターフェイス要素の初期設定のブラウザフォーカスハイライトを無効にするには、ビューアのスタイルシートに次のCSSセレクターを追加します。

```
.s7flyoutviewer *:focus { 
 outline: none; 
}
```

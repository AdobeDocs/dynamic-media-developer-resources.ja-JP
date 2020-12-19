---
description: フォーカスされたビューアのユーザインターフェイス要素の周りに表示される入力フォーカスハイライトは、CSSクラスセレクターを使用して制御します。
seo-description: フォーカスされたビューアのユーザインターフェイス要素の周りに表示される入力フォーカスハイライトは、CSSクラスセレクターを使用して制御します。
seo-title: フォーカスハイライト
solution: Experience Manager
title: フォーカスハイライト
topic: Dynamic media
uuid: 99d822b5-29ea-4229-8eb8-e3903322b7fa
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---


# フォーカスハイライト{#focus-highlight}

フォーカスされたビューアのユーザインターフェイス要素の周りに表示される入力フォーカスハイライトは、CSSクラスセレクターを使用して制御します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSSプロパティ**

外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7video360viewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> outline  </span> </p> </td> 
   <td colname="col2"> <p>フォーカスのハイライトのスタイル </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — ビューアのすべてのユーザインターフェイス要素の初期設定のブラウザフォーカスハイライトを無効にするには、ビューアのスタイルシートに次のCSSセレクターを追加します。

```
.s7video360viewer *:focus { 
 outline: none; 
}
```


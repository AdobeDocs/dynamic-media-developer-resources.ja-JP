---
description: フォーカスされたビューアのユーザインターフェイス要素の周りに表示される入力フォーカスハイライトは、CSSクラスセレクターを使用して制御します。
seo-description: フォーカスされたビューアのユーザインターフェイス要素の周りに表示される入力フォーカスハイライトは、CSSクラスセレクターを使用して制御します。
seo-title: フォーカスハイライト
solution: Experience Manager
title: フォーカスハイライト
topic: Dynamic Media
uuid: 44057e10-98b6-4316-bf6c-9bf569be6a50
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
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
.s7interactivevideoviewer *:focus
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
.s7interactivevideoviewer *:focus { 
 outline: none; 
}
```


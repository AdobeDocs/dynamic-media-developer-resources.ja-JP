---
description: フォーカスされたビューアのUI要素の周りに表示される入力フォーカスハイライトは、CSSクラスセレクターを使用して制御します。
seo-description: フォーカスされたビューアのUI要素の周りに表示される入力フォーカスハイライトは、CSSクラスセレクターを使用して制御します。
seo-title: フォーカスハイライト
solution: Experience Manager
title: フォーカスハイライト
uuid: 81bf9937-6a26-4f69-838e-5ba41608ac09
feature: Dynamic Mediaクラシック，ビューア，SDK/API，スピンセット
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# フォーカスハイライト{#focus-highlight}

フォーカスされたビューアのUI要素の周りに表示される入力フォーカスハイライトは、CSSクラスセレクターを使用して制御します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSSプロパティ**

外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7spinviewer *:focus
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
.s7spinviewer *:focus { 
 outline: none; 
}
```


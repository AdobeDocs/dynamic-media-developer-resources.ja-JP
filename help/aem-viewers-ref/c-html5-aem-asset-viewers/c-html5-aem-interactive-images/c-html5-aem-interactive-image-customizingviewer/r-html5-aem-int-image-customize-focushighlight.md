---
description: フォーカスされたビューアのUI要素の周りに表示される入力フォーカスハイライトは、CSSクラスセレクターを使用して制御します。
solution: Experience Manager
title: フォーカスハイライト
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブ画像
role: 開発者、業務従事者
exl-id: 89f34a96-2b21-4169-8c25-4b53005e59b8
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 1%

---

# フォーカスハイライト{#focus-highlight}

フォーカスされたビューアのUI要素の周りに表示される入力フォーカスハイライトは、CSSクラスセレクターを使用して制御します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSSプロパティ**

外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7interactiveimage *:focus
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
.s7interactiveimage *:focus { 
 outline: none; 
}
```

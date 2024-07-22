---
title: フォーカスのハイライト
description: フォーカスされたビューア UI 要素の周囲に表示される入力フォーカスハイライトは、CSS クラスセレクターで制御します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2cb2e719-ee56-45e5-a509-7e13bb3c2165
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# フォーカスのハイライト{#focus-highlight}

フォーカスされたビューア UI 要素の周囲に表示される入力フォーカスハイライトは、CSS クラスセレクターで制御します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS プロパティ**

外観は、次の CSS クラスセレクターで制御します。

```
.s7flyoutviewer *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 概要 </span> </p> </td> 
   <td colname="col2"> <p>フォーカスハイライトのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – すべてのビューアのユーザーインターフェイス要素に対してデフォルトのブラウザーフォーカスハイライトを無効にするには、次の CSS セレクターをビューアのスタイルシートに追加します。

```
.s7flyoutviewer *:focus { 
 outline: none; 
}
```

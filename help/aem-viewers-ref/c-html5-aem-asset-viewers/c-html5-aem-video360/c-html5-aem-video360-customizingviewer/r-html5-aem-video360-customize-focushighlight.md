---
title: フォーカスのハイライト
description: フォーカスされたビューアのユーザーインターフェイス要素の周囲に表示される入力フォーカスハイライトは、CSS クラスセレクターで制御します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 05ac1a70-c20d-4ddf-942c-181f101cb1d8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 1%

---

# フォーカスのハイライト{#focus-highlight}

フォーカスされたビューアのユーザーインターフェイス要素の周囲に表示される入力フォーカスハイライトは、CSS クラスセレクターで制御します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS プロパティ**

外観は、次の CSS クラスセレクターで制御します。

```
.s7video360viewer *:focus
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
.s7video360viewer *:focus { 
 outline: none; 
}
```

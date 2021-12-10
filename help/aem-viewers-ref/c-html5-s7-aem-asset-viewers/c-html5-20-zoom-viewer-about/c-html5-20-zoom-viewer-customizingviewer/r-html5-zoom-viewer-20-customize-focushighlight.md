---
title: フォーカスのハイライト
description: フォーカスされたビューアの UI 要素の周囲に表示される入力フォーカスハイライトは、CSS クラスセレクターを使用して制御します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 31fd8022-0072-4a4c-8947-57858a094f3c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# フォーカスのハイライト{#focus-highlight}

フォーカスされたビューアの UI 要素の周囲に表示される入力フォーカスハイライトは、CSS クラスセレクターを使用して制御します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS プロパティ**

外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7zoomviewer *:focus
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
   <td colname="col2"> <p>フォーカスのハイライトのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — すべてのビューアユーザインターフェイス要素の初期設定のブラウザフォーカスハイライトを無効にするには、ビューアのスタイルシートに次の CSS セレクターを追加します。

```
.s7zoomviewer *:focus { 
 outline: none; 
}
```

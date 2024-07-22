---
title: フォーカスのハイライト
description: フォーカスされたビューアの使用インターフェイス要素の周囲に表示される入力フォーカスハイライトは、CSS クラスセレクターで制御されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 74ff9669-d56b-4731-9d4a-dda7c831e162
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# フォーカスのハイライト{#focus-highlight}

フォーカスされたビューアの使用インターフェイス要素の周囲に表示される入力フォーカスハイライトは、CSS クラスセレクターで制御されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

外観は、次の CSS クラスセレクターで制御します。

```
.s7basiczoomviewer *:focus
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
.s7basiczoomviewer *:focus { 
 outline: none; 
}
```

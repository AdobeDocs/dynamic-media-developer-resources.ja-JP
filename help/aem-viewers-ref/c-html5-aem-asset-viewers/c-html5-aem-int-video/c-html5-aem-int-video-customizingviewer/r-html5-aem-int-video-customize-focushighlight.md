---
description: フォーカスされたビューアのユーザインターフェイス要素の周囲に表示される入力フォーカスのハイライトは、CSSクラスセレクターを使用して制御します。
solution: Experience Manager
title: フォーカスハイライト
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブビデオ
role: Developer,Business Practitioner
exl-id: cb5231ed-106a-444f-aac7-06dd1a84a665
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 1%

---

# フォーカスハイライト{#focus-highlight}

フォーカスされたビューアのユーザインターフェイス要素の周囲に表示される入力フォーカスのハイライトは、CSSクラスセレクターを使用して制御します。

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
   <td colname="col1"> <p> <span class="codeph"> アウトライン  </span> </p> </td> 
   <td colname="col2"> <p>フォーカスハイライトのスタイル。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — すべてのビューアユーザインターフェイス要素の初期設定のブラウザフォーカスハイライトを無効にするには、ビューアのスタイルシートに次のCSSセレクターを追加します。

```
.s7interactivevideoviewer *:focus { 
 outline: none; 
}
```

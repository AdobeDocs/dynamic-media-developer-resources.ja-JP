---
title: ツールチップ
description: デスクトップシステムでは、ボタンなどの一部のユーザーインターフェイス要素に、マウスポインターを置いたときにツールチップが表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# ツールチップ{#tooltips}

デスクトップシステムでは、ボタンなどの一部のユーザーインターフェイス要素に、マウスポインターを置いたときにツールチップが表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

ツールチップの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線の色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 背景色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>テキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>テキストのフォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>テキストのフォントサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>埋め込み Web ページ内からツールチップスタイルをカスタマイズする場合、すべてのプロパティに `!IMPORTANT` ルール。 ビューアの CSS ファイルでツールチップがカスタマイズされている場合、このルールは不要です。

例 — 角丸の半径が 3 ピクセルのグレーの境界線、背景が黒、Arial®で書き込まれた白のテキストを含むツールチップを設定するには、次のように記述します。

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```

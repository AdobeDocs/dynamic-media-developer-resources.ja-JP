---
title: ツールチップ
description: デスクトップシステムでは、ボタンなどの一部のユーザーインターフェイス要素に、マウスのカーソルを合わせたときに表示されるツールヒントがあります。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0350bdbc-3e3d-4bc0-98f6-5d7bf4121d9a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# ツールチップ{#tooltips}

デスクトップシステムでは、ボタンなどの一部のユーザーインターフェイス要素に、マウスのカーソルを合わせたときに表示されるツールヒントがあります。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

ツールチップの外観は、次の CSS クラスセレクターで制御します。

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
   <td colname="col2"> <p> 背景境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線のカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> 背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>テキストのカラー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリーの </span> </p> </td> 
   <td colname="col2"> <p>テキストフォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>テキストのフォントサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>埋め込む web ページ内からツールヒントのスタイルをカスタマイズする場合、すべてのプロパティにルールを含める必要 `!IMPORTANT` あります。 ビューアの CSS ファイルでツールヒントがカスタマイズされている場合、このルールは必要ありません。

例 – 3 ピクセルの角丸の半径を持つグレーの境界線、黒の背景、Arial® で書かれた白いテキストを持つツールヒントを設定するには、11 ピクセルサイズです。

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

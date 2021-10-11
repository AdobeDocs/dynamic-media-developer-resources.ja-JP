---
title: ツールチップ
description: デスクトップシステムでは、ボタンなどの一部のユーザーインターフェイス要素に、マウスのカーソルを合わせたときに表示されるツールチップが表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 051bfbed-103e-4fcf-9f01-93f03730397a
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# ツールチップ{#tooltips}

デスクトップシステムでは、ボタンなどの一部のユーザーインターフェイス要素に、マウスのカーソルを合わせたときに表示されるツールチップが表示されます。

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
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線の半径 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color  </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線の色 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 背景色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>テキストの色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>テキストのフォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>テキストのフォントサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>埋め込み Web ページ内からツールチップスタイルをカスタマイズする場合は、すべてのプロパティに `!IMPORTANT` ルールを含める必要があります。 ビューアの CSS ファイル内でツールチップをカスタマイズする場合、このルールは必要ありません。

例 — 角丸の半径が 3 ピクセル、背景が黒、テキストが白の灰色の境界線を持つツールチップを Arial®、11 ピクセルで設定するには、次のように記述します。

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

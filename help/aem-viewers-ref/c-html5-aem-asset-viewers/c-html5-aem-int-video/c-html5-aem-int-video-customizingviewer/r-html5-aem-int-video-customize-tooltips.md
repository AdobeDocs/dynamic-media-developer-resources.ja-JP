---
title: ツールチップ
description: デスクトップシステムでは、ボタンなどの一部のユーザインターフェイス要素に、マウスのカーソルを合わせたときに表示されるツールチップがあります。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 430809d8-3d51-49b7-b6bf-c3c3c77501ff
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 3%

---

# ツールチップ{#tooltips}

デスクトップシステムでは、ボタンなどの一部のユーザインターフェイス要素に、マウスのカーソルを合わせたときに表示されるツールチップがあります。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

ツールチップの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線の半径 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color  </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線のカラー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 背景色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>テキストカラー </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>テキストのフォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>テキストのフォントサイズ </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>埋め込みWebページ内からツールチップスタイルをカスタマイズする場合は、すべてのプロパティに`!IMPORTANT`ルールを含める必要があります。 この注意は、ビューアのCSSファイル内でツールチップをカスタマイズする場合は必要ありません。

## 例 {#section-59e009fd05b14019936aba04d7ca779d}

3ピクセルの角丸の半径、黒の背景、白のテキストを持つグレーの境界線を持つツールチップをArial®、11ピクセルで設定するには：

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

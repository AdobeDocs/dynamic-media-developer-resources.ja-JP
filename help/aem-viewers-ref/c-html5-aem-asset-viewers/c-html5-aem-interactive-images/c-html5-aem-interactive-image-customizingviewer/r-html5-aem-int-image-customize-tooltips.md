---
description: デスクトップシステムでは、ボタンなどの一部のユーザインターフェイス要素に、マウスカーソルを合わせたときに表示されるツールヒントがあります。
seo-description: デスクトップシステムでは、ボタンなどの一部のユーザインターフェイス要素に、マウスカーソルを合わせたときに表示されるツールヒントがあります。
seo-title: ツールチップ
solution: Experience Manager
title: ツールチップ
topic: Dynamic media
uuid: 4cf5ce32-136e-4612-b550-715d51cef982
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Tooltips{#tooltips}

デスクトップシステムでは、ボタンなどの一部のユーザインターフェイス要素に、マウスカーソルを合わせたときに表示されるツールヒントがあります。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

ツールヒントの外観は、以下のCSSクラスセレクターを使用して制御します。

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
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線の半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> 背景の境界線の色 </p> </td> 
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
   <td colname="col2"> <p>テキストのフォントサイズ </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>埋め込みWebページ内からツールヒントのスタイルをカスタマイズする場合は、すべてのプロパティにルールを含める必要が `!IMPORTANT` あります。 これは、ツールヒントがビューアのCSSファイルでカスタマイズされている場合は不要です。

例 — 角丸の半径が3ピクセル、背景が黒、サイズが11ピクセルのArialの白の境界線がグレーのツールヒントを設定するには、次のように記述します。

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


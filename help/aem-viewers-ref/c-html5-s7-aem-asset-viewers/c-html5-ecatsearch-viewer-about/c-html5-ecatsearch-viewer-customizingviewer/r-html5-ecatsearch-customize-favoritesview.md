---
description: お気に入りビューは、サムネール画像の列で構成されます。
seo-description: お気に入りビューは、サムネール画像の列で構成されます。
seo-title: お気に入りビュー
solution: Experience Manager
title: お気に入りビュー
topic: Dynamic media
uuid: e9d0380e-3b08-45e4-8419-447df2e8de37
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# お気に入りビュー{#favorites-view}

お気に入りビューは、サムネール画像の列で構成されます。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

お気に入りビューのコンテナの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7favoritesview
```

お気に入りビューの位置と高さは、ビューによって管理されます。cssでは、幅のみを定義できます。

**お気に入りビューのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> お気に入りビューの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ビューの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 幅が100ピクセルで、背景色が半透明のグレーのお気に入りビューを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

お気に入りサムネールの間隔は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**お気に入りサムネールのCSSプロパティ**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周囲の垂直方向のマージンのサイズ。 実際のサムネールの間隔は、.s7thumbcellに設定された上下のマージンの合計 <span class="codeph"> になります </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 10ピクセルの間隔を設定します。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

個々のサムネールの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**お気に入りサムネールのCSSプロパティ**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p>サムネールの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムネールでは、属性セ `state` レクターがサポートされます。このセレクターは、サムネールの状態ごとに異なるスキンを適用するのに使用できます。 特に、は、ユーザ `state="selected"` ーが最近選択したサムネールに対応します。 `state="default"` は、残りのサムネールに対応します。 また、マウ `state="over"` スのカーソルを合わせたときに使用されます。

例 — 75 x 75ピクセルで、初期設定の境界線がライトグレーで、選択した境界線がダークグレーのサムネールを設定します。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

サムネールラベルの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**お気に入りラベルのCSSプロパティ**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリ </span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 14ピクセルのHelveticaフォントのラベルを設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```


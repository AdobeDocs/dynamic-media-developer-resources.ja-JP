---
description: お気に入りビューは、サムネール画像の列で構成されます。
solution: Experience Manager
title: お気に入りビュー
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 10536242-1015-49ff-ae27-59671f30d886
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---

# お気に入りビュー{#favorites-view}

お気に入りビューは、サムネール画像の列で構成されます。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

お気に入りビューコンテナの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7favoritesview
```

お気に入りビューの位置と高さは、ビューで管理されます。CSSでは、幅の定義のみ可能です。

**お気に入りビューのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
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
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

お気に入りサムネールの間隔は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**お気に入りサムネールのCSSプロパティ**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周囲の垂直方向のマージンのサイズ。 実際のサムネールの間隔は、 <span class="codeph"> .s7thumbcell </span>に設定された上下のマージンの合計になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 10ピクセル間隔を設定します。

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

個々のサムネールの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**お気に入りサムネールのCSSプロパティ**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
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
>サムネールでは、 `state`属性セレクターがサポートされます。このセレクターは、サムネールの状態ごとに異なるスキンを適用するのに使用できます。 特に、`state="selected"`は、ユーザーが最近選択したサムネールに対応します。 `state="default"` は、残りのサムネールに対応します。`state="over"`はマウスポインターを置くと使用されます。

例 — 75 x 75ピクセルで、初期設定の境界線がライトグレー、選択された境界線がダークグレーのサムネールを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

サムネールラベルの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**お気に入りラベルのCSSプロパティ**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-famiy  </span> </p> </td> 
   <td colname="col2"> <p>フォント名 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 14ピクセルのHelveticaフォントを使用するラベルを設定します。

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

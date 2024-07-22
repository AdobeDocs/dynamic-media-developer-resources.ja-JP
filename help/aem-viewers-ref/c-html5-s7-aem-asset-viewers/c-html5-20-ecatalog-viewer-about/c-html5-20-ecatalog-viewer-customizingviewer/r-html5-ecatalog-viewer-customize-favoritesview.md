---
title: お気に入り表示
description: お気に入り表示は、サムネール画像の列で構成されています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# お気に入り表示{#favorites-view}

お気に入り表示は、サムネール画像の列で構成されています。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

お気に入り表示コンテナの外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogviewer .s7favoritesview
```

お気に入りビューの位置と高さはビューで管理されます。CSS では、幅の定義のみ可能です。

**お気に入りビューの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> [ お気に入り ] ビューの背景色 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>ビューの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 幅 100 ピクセルのお気に入りビューを半透明のグレーの背景で設定するには：

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

お気に入りのサムネール間の間隔は、次の CSS クラスセレクターで制御されます。

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**お気に入りのサムネールの CSS プロパティ**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの周囲の垂直方向の余白のサイズ。 実際のサムネールの間隔は、.s7thumbcell </span> に設定されている上下の余白 <span class="codeph"> 合計と等しくなります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 10 ピクセル間隔を設定するには：

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

個々のサムネールの外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**お気に入りのサムネールの CSS プロパティ**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 境界線 </span> </p> </td> 
   <td colname="col2"> <p>サムネールのボーダー。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムネールでは `state` 属性セレクターがサポートされており、これを使用して異なるスキンを異なるサムネール状態に適用できます。 特に、`state="selected"` は、ユーザーが最近選択したサムネールに対応します。 残りのサムネールに対応する属性 `state="default"`。 また、属性 `state="over"` は、マウスのカーソルを合わせたときに使用されます。

例 – 75 x 75 ピクセルのサムネールで、デフォルトの境界線が薄いグレーで、選択した境界線が濃いグレーになるように設定するには：

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

サムネールラベルの外観は、次の CSS クラスセレクターで制御します。

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**お気に入りラベルの CSS プロパティ**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-famiy </span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 14 ピクセルの Helvetica® フォントでラベルを設定するには：

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

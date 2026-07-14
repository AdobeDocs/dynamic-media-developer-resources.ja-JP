---
title: お気に入りビュー
description: お気に入りビューは、サムネール画像の列で構成されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 8daf3d19-615b-4d62-a6f5-6a153d193b88
TQID: 'https://experienceleague.adobe.com/2VO3PqMcaxByTVGi0NG3TtqPKszOSkeYK4uxBVG3ixM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# お気に入りビュー{#favorites-view}

お気に入りビューは、サムネール画像の列で構成されます。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

お気に入りビューコンテナの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7favoritesview
```

お気に入りビューの位置と高さは、ビューによって管理されます。CSSでは、幅を定義することしかできません。

**お気に入りビューのCSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> お気に入りビューの背景色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>ビューの幅。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 半透明の灰色の背景を持つ、幅100 ピクセルのお気に入りビューを設定する。

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

お気に入りのサムネールの間隔は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**お気に入りのサムネールのCSS プロパティ**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> マージン </span> </p> </td> 
   <td colname="col2"> <p> 各サムネールの垂直余白のサイズ。 実際のサムネールの間隔は、<span class="codeph"> .s7thumbcell </span>に設定されている上下の余白の合計と同じです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 10 ピクセル間隔を設定します。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

個々のサムネールの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**お気に入りのサムネールのCSS プロパティ**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>サムネールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>サムネールの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p>サムネールの境界線。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>サムネールは`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるサムネール状態に異なるスキンを適用できます。 特に、`state="selected"`は、ユーザーが最近選択したサムネールに対応しています。 `state="default"`は残りのサムネールに対応していますが、 `state="over"`はマウスオーバーで使用されます。

例 – 75 x 75 ピクセルのサムネールを設定するには、明るいグレーのデフォルトの境界線と、濃いグレーの選択した境界線があります。

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

サムネールラベルの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**お気に入りラベルのCSS プロパティ**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントファミリー</span> </p> </td> 
   <td colname="col2"> <p>フォント名。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フォントサイズ </span> </p> </td> 
   <td colname="col2"> <p>フォントサイズ： </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 14 ピクセルのHelvetica® フォントでラベルを設定する。

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

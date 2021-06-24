---
description: ビューアでは、メインビューの上のお気に入りアイコンが、ユーザが最初に追加した場所に表示されます。
solution: Experience Manager
title: お気に入りエフェクト
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# お気に入りエフェクト{#favorites-effect}

ビューアでは、メインビューの上のお気に入りアイコンが、ユーザが最初に追加した場所に表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

お気に入りアイコンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**お気に入りアイコンのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> アイコンに表示する画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSSスプライト</a>も参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>アイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>アイコンの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 36 x 36ピクセルのお気に入りアイコンを設定します。

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

デスクトップシステムでは、コンポーネントは`cursortype`属性セレクターをサポートします。このセレクターは`.s7favoriteseffect`クラスに適用でき、選択したユーザーアクションに基づいてカーソルのタイプを制御します。 次の`cursortype`値がサポートされています。

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add  </span> </p> </td> 
   <td colname="col2"> <p>新しいお気に入りアイコンを追加中のユーザーが表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove  </span> </p> </td> 
   <td colname="col2"> <p>表示されたユーザーは、既存のお気に入りアイコンを削除しています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view  </span> </p> </td> 
   <td colname="col2"> <p>[お気に入り]編集がアクティブでない場合、通常の操作モードで表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — コンポーネントの状態ごとに異なるマウスカーソルを設定します。

```
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```

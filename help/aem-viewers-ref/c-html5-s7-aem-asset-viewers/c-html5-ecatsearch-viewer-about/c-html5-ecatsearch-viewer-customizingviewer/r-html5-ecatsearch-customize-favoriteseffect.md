---
description: メインビューの上に、ユーザが最初に追加した場所にお気に入りアイコンが表示されます。
seo-description: メインビューの上に、ユーザが最初に追加した場所にお気に入りアイコンが表示されます。
seo-title: お気に入りエフェクト
solution: Experience Manager
title: お気に入りエフェクト
topic: Dynamic media
uuid: 5fbfe299-1fae-427f-8ade-e12cd168b8a7
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# お気に入りエフェクト{#favorites-effect}

メインビューの上に、ユーザが最初に追加した場所にお気に入りアイコンが表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

お気に入りアイコンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

**お気に入りアイコンのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> アイコンに対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p>CSSスプライトも参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 照してくださ </a>い。 </p> </td> 
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
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

デスクトップシステムでは、コンポーネントは、 `cursortype` クラスに適用できる属性セレクターをサポートし、選択し `.s7favoriteseffect` たユーザーアクションに基づいてカーソルのタイプを制御します。 The following `cursortype` values are supported:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>表示されたユーザが新しいお気に入りアイコンを追加しようとしています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>表示されたユーザーが既存のお気に入りアイコンを削除しています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>お気に入りの編集がアクティブでない場合に、通常の操作モードで表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — コンポーネントの状態のタイプごとに異なるマウスカーソルを使用します。

```
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```


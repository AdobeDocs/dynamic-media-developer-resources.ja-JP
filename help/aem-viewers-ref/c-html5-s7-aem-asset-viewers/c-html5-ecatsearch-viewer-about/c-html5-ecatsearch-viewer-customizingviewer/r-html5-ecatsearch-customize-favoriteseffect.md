---
title: お気に入りエフェクト
description: ビューアには、ユーザーが最初に追加した場所に、メインビュー上にお気に入りアイコンが表示されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 7603c873-a2d1-4a24-85a6-8e56a1f207de
TQID: 'https://experienceleague.adobe.com/BRm7DkWXxfUao0dvoWOvhNF605lnuZfJsyKvlB7Rhb8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 182
ht-degree: 0%

---

# お気に入りエフェクト{#favorites-effect}

ビューアには、ユーザーが最初に追加した場所に、メインビュー上にお気に入りアイコンが表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

お気に入りアイコンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

お気に入りアイコンの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> アイコンに表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>アイコンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>アイコンの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 36 x 36 ピクセルのお気に入りアイコンを設定します。

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

デスクトップシステムでは、コンポーネントは`.s7favoriteseffect` クラスに適用できる`cursortype`属性セレクターをサポートし、選択したユーザーアクションに基づいてカーソルの種類を制御します。 次の`cursortype`値がサポートされています：

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>表示されているユーザーは、新しいお気に入りアイコンを追加しています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>表示されているユーザーは、既存のお気に入りアイコンを削除しています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>お気に入り編集がアクティブでない場合、通常の操作モードで表示されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – コンポーネントの状態のタイプごとに異なるマウスカーソルを使用します。

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


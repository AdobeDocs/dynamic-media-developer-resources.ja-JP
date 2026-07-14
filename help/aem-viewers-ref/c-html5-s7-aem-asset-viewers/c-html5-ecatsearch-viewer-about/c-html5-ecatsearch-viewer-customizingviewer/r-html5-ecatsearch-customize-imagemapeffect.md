---
title: 画像マップエフェクト
description: モードパラメーターの値に応じて、ビューアは、Dynamic Media Classicでマップが作成された場所に画像マップアイコンをメインビュー上に表示したり、元の画像マップの形状に一致する正確なリージョンをレンダリングしたりします。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 873fc387-1d2a-4d74-b85e-fcbb13b691c5
TQID: 'https://experienceleague.adobe.com/cG9m71LkGsy3wqj16qS-pvskuP6J-XrF93jog28I62c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 0%

---

# 画像マップエフェクト{#image-map-effect}

モードパラメーターの値に応じて、ビューアは、Dynamic Media Classicでマップが作成された場所に画像マップアイコンをメインビュー上に表示したり、元の画像マップの形状に一致する正確なリージョンをレンダリングしたりします。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

メイン ビューア領域の&#x200B;**CSS プロパティ**

画像マップアイコンの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>過去に画像マップアイコンのスタイル設定に使用されていた`s7mapoverlay` CSS クラスは現在では非推奨です。代わりに`s7icon`を使用してください。

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンの幅（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>画像マップ アイコンの高さ（ピクセル単位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>画像マップアイコンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、様々なスキンを`default`と`active`のアイコン状態に適用できます。

例 – 28 x 28 ピクセルの画像マップアイコンを設定し、2つの異なるアイコンの状態ごとに異なる画像を表示します。

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

[画像マップのサポート ](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)も参照してください。

画像マップ領域のアピアランスは、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景</span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の塗りつぶしカラー。 </p> <p>#RRGGBB、RGB（R,G,B）またはRGBA （R,G,B,A）フォーマットで指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の塗りつぶしカラー。 </p> <p>#RRGGBB、RGB（R,G,B）またはRGBA （R,G,B,A）フォーマットで指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">境界線</span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の境界線スタイル。 </p> <p><span class="codeph"> <span class="varname"> width </span> solid <span class="varname"> color </span> </span>として指定されます。ここで、<span class="codeph"> <span class="varname"> width </span> </span>はピクセルで表され、<span class="codeph"> <span class="varname"> color </span> </span>は#RRGGBB、RGB（R,G,B）またはRGBA （R,G,B,A）として設定されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – `1` ピクセルの黒い境界線を持つ透明な画像マップ領域を設定します。

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```


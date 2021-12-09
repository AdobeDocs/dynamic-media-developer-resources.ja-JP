---
description: mode パラメーターの値に応じて、ビューアは、Dynamic Media Classicでマップが最初に作成された場所のメインビュー上に画像マップアイコンを表示します。 または、元の画像マップの形状と一致する正確な領域をレンダリングします。
solution: Experience Manager
title: 画像マップ効果
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3816118f-4eb7-4436-9f54-155dde077734
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---

# 画像マップ効果{#image-map-effect}

mode パラメーターの値に応じて、ビューアは、Dynamic Media Classicでマップが最初に作成された場所のメインビュー上に画像マップアイコンを表示します。 または、元の画像マップの形状と一致する正確な領域をレンダリングします。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

画像マップアイコンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>この `s7mapoverlay` 以前に画像マップアイコンのスタイル設定に使用されていた CSS クラスは、非推奨（廃止予定）となりました。use `s7icon` 代わりに、

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンの幅（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>画像マップアイコンの高さ（ピクセル単位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>画像マップアイコンは、 `state` 属性セレクター。このセレクターを使用して、アイコンの状態に応じて異なるスキンを適用できます。 `default` および `active`.

例 — 28 x 28 ピクセルで、2 つの異なるアイコン状態ごとに異なる画像を表示する画像マップアイコンを設定します。

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

関連トピック [画像マップのサポート](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

画像マップ領域の外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7imagemapeffect .s7region
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
   <td colname="col1"> <p> <span class="codeph"> 背景 </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の塗りのカラー。 </p> <p>#RRGGBB、RGB(R,G,B) または RGBA(R,G,B,A) 形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の塗りのカラー。 </p> <p>#RRGGBB、RGB(R,G,B) または RGBA(R,G,B,A) 形式で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 枠線 </span> </p> </td> 
   <td colname="col2"> <p> 画像マップ領域の境界線のスタイル。 </p> <p>指定形式 <span class="codeph"> <span class="varname"> 幅 </span> 実線 <span class="varname"> カラー </span> </span>で、 <span class="codeph"> <span class="varname"> 幅 </span> </span> はピクセル単位で表され、 <span class="codeph"> <span class="varname"> カラー </span> </span> は#RRGGBB、RGB(R,G,B) または RGBA(R,G,B,A) として設定されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 透明な画像マップ領域を `1` ピクセルの黒い境界線：

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

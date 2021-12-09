---
title: アイコンエフェクト
description: ズームインジケーターは、メインビュー領域に重ねて表示されます。 画像がリセット状態のときに表示され、iconeffect パラメーターの設定にも依存します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: fee22d02-172c-4f82-9b6c-e06db530f400
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---

# アイコンエフェクト{#icon-effect}

ズームインジケーターは、メインビュー領域に重ねて表示されます。 画像がリセット状態のときに表示され、iconeffect パラメーターの設定にも依存します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

表示領域の外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7pageview .s7iconeffect
```

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
   <td colname="col2"> <p> ズームインジケーターのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ズームインジケーターの幅（ピクセル単位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ズームインジケーターの高さ（ピクセル単位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>アイコンエフェクトは、 `media-type` 属性セレクターを使用します。このセレクターを使用すると、デバイスごとに異なるアイコンエフェクトを適用できます。 特に `media-type='standard'` マウス入力が通常使用されるデスクトップシステムに対応し、 `media-type='multitouch'` は、タッチ入力のデバイスに対応します。

例 — デスクトップシステムとタッチデバイス用に、異なるアートを持つ 100 x 100 ピクセルのズームインジケーターを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7pageview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```

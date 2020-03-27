---
description: ズームインジケータは、ズームビュー領域に重ねて表示されます。 画像がリセット状態の場合に表示され、iconeffectパラメーターの設定によっても表示されます。
seo-description: ズームインジケータは、ズームビュー領域に重ねて表示されます。 画像がリセット状態の場合に表示され、iconeffectパラメーターの設定によっても表示されます。
seo-title: ズームビューアイコンエフェクト
solution: Experience Manager
title: ズームビューアイコンエフェクト
topic: Dynamic media
uuid: 69a44789-9587-4459-9c75-048773c9e368
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# ズームビューアイコンエフェクト{#zoom-view-icon-effect}

ズームインジケータは、ズームビュー領域に重ねて表示されます。 画像がリセット状態の場合に表示され、iconeffectパラメーターの設定によっても表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
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
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p>CSSスプライ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> トを参照してくだ </a>さい。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ズームインジケータの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ズームインジケータの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>アイコンエフェクトでは、属 `media-type` 性セレクターがサポートされます。このセレクターを使用して、異なるデバイスに異なるアイコンエフェクトを適用できます。 特に、は、マウス入 `media-type='standard'` 力が通常使用されるデスクトップシステムに対応し、タッチ入力 `media-type='multitouch'` を使用するデバイスに対応します。

例 — デスクトップシステムとタッチデバイスで異なるアートを使用する100 x 100ピクセルのズームインジケーターを設定するには、次のように記述します。

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```


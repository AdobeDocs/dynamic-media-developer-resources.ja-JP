---
description: ズームインジケーターは、ズームビュー領域に重ねて表示されます。 これは画像がリセット状態のときに表示され、 iconeffectパラメーターの設定にも依存します。
solution: Experience Manager
title: ズームビューのアイコンエフェクト
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: f2db0259-f1cf-41bc-86fd-97a40d01db16
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# ズームビューのアイコンエフェクト{#zoom-view-icon-effect}

ズームインジケーターは、ズームビュー領域に重ねて表示されます。 これは画像がリセット状態のときに表示され、 iconeffectパラメーターの設定にも依存します。

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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> ズームインジケーターのアートワーク </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合の、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ズームインジケーターの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ズームインジケーターの高さ </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>アイコンエフェクトでは、`media-type`属性セレクターがサポートされます。このセレクターを使用して、デバイスごとに異なるアイコンエフェクトを適用できます。 特に、`media-type='standard'`は、マウス入力が通常使用されるデスクトップシステムに対応し、`media-type='multitouch'`はタッチ入力を使用するデバイスに対応します。

例 — デスクトップシステムとタッチデバイス用に、異なるアートを持つ100 x 100ピクセルのズームインジケーターを設定するには、次のように記述します。

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

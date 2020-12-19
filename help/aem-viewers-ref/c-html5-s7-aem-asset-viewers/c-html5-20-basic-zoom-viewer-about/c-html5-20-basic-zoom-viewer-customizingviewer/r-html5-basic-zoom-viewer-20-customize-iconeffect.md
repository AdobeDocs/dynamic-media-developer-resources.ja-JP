---
description: ズームインジケーターは、メイン表示領域に重ねて表示されます。 画像がリセット状態の場合に表示されます。また、iconeffectパラメーターの設定によって表示されます。
seo-description: ズームインジケーターは、メイン表示領域に重ねて表示されます。 画像がリセット状態の場合に表示されます。また、iconeffectパラメーターの設定によって表示されます。
seo-title: アイコンエフェクト
solution: Experience Manager
title: アイコンエフェクト
topic: Dynamic media
uuid: 113b2502-395d-4fd1-ab28-4995e8248593
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# アイコンエフェクト{#icon-effect}

ズームインジケーターは、メイン表示領域に重ねて表示されます。 画像がリセット状態の場合に表示されます。また、iconeffectパラメーターの設定によって表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7basiczoomviewer .s7zoomview .s7iconeffect
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
   <td colname="col2"> <p> ズームインジケーターのアートワーク。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ズームインジケーターの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ズームインジケーターの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>アイコンエフェクトでは、`media-type`属性セレクターがサポートされます。このセレクターを使用すると、デバイスごとに異なるアイコンエフェクトを適用できます。 特に、`media-type='standard'`はマウス入力が通常使用されるデスクトップシステムに対応し、`media-type='multitouch'`はタッチ入力のデバイスに対応します。

例 — デスクトップシステムとタッチデバイスで別々のアートを使用する100 x 100ピクセルのズームインジケーターを設定するには、次のように記述します。

```
.s7basiczoomviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7basiczoomviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7basiczoomviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```


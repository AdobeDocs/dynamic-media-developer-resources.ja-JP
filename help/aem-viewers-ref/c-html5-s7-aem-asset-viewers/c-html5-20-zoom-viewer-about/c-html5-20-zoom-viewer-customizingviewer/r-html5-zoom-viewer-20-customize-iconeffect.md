---
description: ズームインジケーターは、メイン表示領域に重ねて表示されます。 画像がリセット状態の場合に表示されます。また、iconeffectパラメーターの設定によって表示されます。
seo-description: ズームインジケーターは、メイン表示領域に重ねて表示されます。 画像がリセット状態の場合に表示されます。また、iconeffectパラメーターの設定によって表示されます。
seo-title: アイコンエフェクト
solution: Experience Manager
title: アイコンエフェクト
uuid: 5daf15ec-fcc5-4e37-924e-9a2cd6c0d167
feature: Dynamic Mediaクラシック，ビューア，SDK/API，ズーム
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---


# アイコンエフェクト{#icon-effect}

ズームインジケーターは、メイン表示領域に重ねて表示されます。 画像がリセット状態の場合に表示されます。また、iconeffectパラメーターの設定によって表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

表示領域の外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7zoomviewer .s7zoomview .s7iconeffect
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
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSSスプライト</a>を参照してください。 </p> </td> 
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
.s7zoomviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7zoomviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7zoomviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```


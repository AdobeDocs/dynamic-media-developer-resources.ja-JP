---
title: フルスクリーンボタン
description: 全画面ボタンをクリックすると、ユーザーが全画面モードに入るか終了します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 0cb2b1bd-154e-41d8-bd9f-69a1cfc72902
TQID: 'https://experienceleague.adobe.com/BpxjsHa7DW5c4PhOEwFsoFydVj4aZGTLEBy0f3W8tf4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 255
ht-degree: 0%

---

# フルスクリーンボタン{#full-screen-button}

全画面ボタンをクリックすると、ユーザーが全画面モードに入るか終了します。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

フルスクリーンボタンを含むコントロールバーに対して、CSSでサイズ調整、スキン調整、位置を調整できます。

フルスクリーンボタンのアピアランスは、CSS クラスセレクターで制御します。

```
.s7video360viewer .s7fullscreenbutton
```

フルスクリーンボタンの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上位</span> </p> </td> 
   <td colname="col2"> <p> パディングを含む上部境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p> パディングを含む右端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">さんが</span>を残しました </p> </td> 
   <td colname="col2"> <p> パディングを含む左端からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下</span> </p> </td> 
   <td colname="col2"> <p>パディングを含む下部境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> フルスクリーンボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>フルスクリーンボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態の表示画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS スプライト </a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`と`selected`の両方の属性セレクターをサポートしており、異なるスキンを異なるボタンの状態に適用するために使用できます。 特に、`selected='true'`は「フルスクリーン」状態に対応し、`selected='false'`は「通常」状態に対応します。

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)を参照してください。

**例** - コントロールバーの上端と右端から6 ピクセル配置された32 x 32 ピクセルのフルスクリーンボタンを設定します。 また、4つの異なるボタンの状態ごとに異なる画像を表示します。

```
.s7video360viewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7video360viewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7video360viewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

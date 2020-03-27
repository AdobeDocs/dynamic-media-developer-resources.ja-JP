---
description: フルスクリーンボタンをクリックすると、ビューアのフルスクリーンモードが開始または終了します。 ビューアがビデオを表示しているときに使用され、コントロールバーに表示されます。 ビューアがポップアップモードで動作し、システムがネイティブのフルスクリーンをサポートしていない場合、このボタンは表示されません。
seo-description: フルスクリーンボタンをクリックすると、ビューアのフルスクリーンモードが開始または終了します。 ビューアがビデオを表示しているときに使用され、コントロールバーに表示されます。 ビューアがポップアップモードで動作し、システムがネイティブのフルスクリーンをサポートしていない場合、このボタンは表示されません。
seo-title: ビデオのフルスクリーンボタン
solution: Experience Manager
title: ビデオのフルスクリーンボタン
topic: Dynamic media
uuid: f264154b-eb4d-4dcb-b8c0-e06c383198ae
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# ビデオのフルスクリーンボタン{#video-full-screen-button}

フルスクリーンボタンをクリックすると、ビューアのフルスクリーンモードが開始または終了します。 ビューアがビデオを表示しているときに使用され、コントロールバーに表示されます。 ビューアがポップアップモードで動作し、システムがネイティブのフルスクリーンをサポートしていない場合、このボタンは表示されません。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

フルスクリーンボタンのサイズ、スキン、およびこのボタンを含むコントロールバーに対する位置を、CSSで設定できます。

フルスクリーンボタンの外観は、CSSクラスセレクターを使用して制御します。

```
.s7mixedmediaviewer .s7fullscreenbutton
```

**フルスクリーンボタンのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> トップ </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む上の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む右の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左 </span> </p> </td> 
   <td colname="col2"> <p> パディングを含む、左の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下 </span> </p> </td> 
   <td colname="col2"> <p>パディングを含む下の境界線からの位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> フルスクリーンボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>フルスクリーンボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p>CSSスプライ <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> トを参照してくだ </a>さい。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、属性セレクターと属 `state` 性セレク `selected` ターの両方がサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。 特に、は「フ `selected='true'` ルスクリーン」状態に対応し、「 `selected='false'` 通常」状態に対応します。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザインターフェイス要素のローカリゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) を参照してください。

## 例 {#section-e8caea0a303c425a8a637c2a47c06355}

32 x 32ピクセルで、コントロールバーの上および右端から6ピクセルの位置に配置するフルスクリーンボタンを設定します。 また、選択時または未選択時のボタンの4つの状態ごとに異なる画像を表示します。

```
.s7mixedmediaviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```


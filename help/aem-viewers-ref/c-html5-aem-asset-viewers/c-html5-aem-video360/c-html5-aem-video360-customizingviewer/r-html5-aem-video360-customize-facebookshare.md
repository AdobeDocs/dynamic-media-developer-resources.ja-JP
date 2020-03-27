---
description: Facebook共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 ボタンをクリックすると、ソーシャルサービスによって提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
seo-description: Facebook共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 ボタンをクリックすると、ソーシャルサービスによって提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。
seo-title: Facebook共有
solution: Experience Manager
title: Facebook共有
topic: Dynamic media
uuid: 8575fde4-4d03-4b87-a628-ff06ff8c91c9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Facebook共有{#facebook-share}

Facebook共有ツールは、ソーシャル共有パネルに追加されるボタンで構成されます。 ボタンをクリックすると、ソーシャルサービスによって提供される共有ダイアログボックスにリダイレクトされます。 ボタンの位置は、ソーシャル共有ツールで完全に管理されます。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Facebook共有ボタンの外観は、以下のCSSクラスセレクターを使用して制御します。

```
.s7video360viewer .s7facebookshare
```

**Facebook共有ツールのCSSプロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>ボタンの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ボタンの高さ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 特定のボタンの状態で表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSSスプライトを使用する場合、アートワークスプライト内の位置。 </p> <p>CSSスプライ <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> トを参照してくだ </a>さい。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンでは、属性セレ `state` クターがサポートされます。このセレクターは、ボタンの状態ごとに異なるスキンを適用するのに使用できます。

CSSクラスでCSSプロパティを設定することで、ソーシャル共有パネルからボ `display:none` タンを削除できます。

ボタンのツールチップはローカライズできます。 詳しくは、ユー [ザインターフェイス要素のローカリゼーションを参照してくださ](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)い。

**例** - 28 x 28ピクセルで、ボタンの4つの状態ごとに異なる画像を表示するFacebook共有ボタンを設定するには、次のように記述します。

```
.s7video360viewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7video360viewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7video360viewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7video360viewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```


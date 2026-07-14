---
title: ソーシャル共有
description: ソーシャル共有ツールは、デフォルトで左上隅に表示されます。 ボタンと、オーディエンスがボタンをクリックまたはタップすると展開されるパネルで構成されます。このパネルには、個々の共有ツールが含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5cac6c86-08fb-46fd-bab0-ab77154eb770
TQID: 'https://experienceleague.adobe.com/2rIF-7PJheaFqyDvzu6mUiXzGJol8-KNvuwZlb7eeRc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 335
ht-degree: 0%

---

# ソーシャル共有{#social-share}

ソーシャル共有ツールは、デフォルトで左上隅に表示されます。 ボタンと、オーディエンスがボタンをクリックまたはタップすると展開されるパネルで構成されます。このパネルには、個々の共有ツールが含まれます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビューアユーザーインターフェイスのソーシャル共有ツールの位置とサイズは、次のように制御されます。

```
.s7ecatalogsearchviewer .s7socialshare
```

ソーシャル共有ツールの&#x200B;**CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーの上部からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> 左の次のボタンまでの距離、またはこのボタンが行の最初のボタンの場合はコントロールバーの左側までの距離。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">幅</span> </p> </td> 
   <td colname="col2"> <p> ソーシャル共有ツールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">の高さ</span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツールの高さ。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – ビューアコンテナの上部から4 ピクセル、右側から5 ピクセルの位置に配置され、28 x 28 ピクセルのサイズのソーシャル共有ツールを設定します。

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

ソーシャル共有ツールボタンの表示は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

ソーシャル ボタンの&#x200B;**CSS プロパティ**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景画像</span> </p> </td> 
   <td colname="col2"> <p> 特定のボタン状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>も参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、`state`属性セレクターをサポートしています。このセレクターを使用すると、異なるスキンを異なるボタンの状態に適用できます。

ボタンツールのヒントはローカライズできます。 詳しくは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。

例 – 4つの異なるボタンの状態ごとに異なる画像を表示するソーシャル共有ツールボタンを設定します。

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

個々のソーシャル共有アイコンを含むパネルの外観は、次のCSS クラスセレクターで制御されます。

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
```

ソーシャル共有パネルの&#x200B;**CSS プロパティ**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>パネルの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 – 透明な色を持つパネルを設定します。

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

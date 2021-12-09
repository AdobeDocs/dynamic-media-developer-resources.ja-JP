---
title: ソーシャル共有
description: ソーシャル共有ツールは、デフォルトで左上隅に表示されます。 このツールは、ボタンと、ユーザーがボタンをクリックまたはタップしたときに展開するパネルで構成され、個々の共有ツールが含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b65b8846-3287-47ae-bdb6-6cac768cece0
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# ソーシャル共有{#social-share}

ソーシャル共有ツールは、デフォルトで左上隅に表示されます。 このツールは、ボタンと、ユーザーがボタンをクリックまたはタップしたときに展開するパネルで構成され、個々の共有ツールが含まれます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

ビューアのユーザーインターフェイスでのソーシャル共有ツールの位置とサイズは、次の方法で制御します。

```
.s7ecatalogviewer .s7socialshare
```

**ソーシャル共有ツールの CSS プロパティ**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーの上からのオフセット。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> 左側の次のボタンまたは行の最初のボタンの場合はコントロールバーの左側までの距離。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> ソーシャル共有ツールの幅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>ソーシャル共有ツールの高さです。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — ビューアのコンテナの上から 4 ピクセル、右から 5 ピクセルの位置に配置し、サイズが 28 x 28 ピクセルのソーシャル共有ツールを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

ソーシャル共有ツールボタンの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7socialshare .s7socialbutton
```

**ソーシャルボタンの CSS プロパティ**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> ボタンの特定の状態に対して表示される画像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS スプライトを使用する場合は、アートワークスプライト内に配置します。 </p> <p>関連トピック <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS スプライト </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>このボタンは、 `state` 属性セレクター。ボタンの状態ごとに異なるスキンを適用するのに使用できます。

ボタンのツールチップはローカライズできます。 詳しくは、 [ユーザーインターフェイス要素のローカライゼーション](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) を参照してください。

例 — 4 つのボタンの状態ごとに異なる画像を表示するソーシャル共有ツールボタンを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

個々のソーシャル共有アイコンを含むパネルの外観は、以下の CSS クラスセレクターを使用して制御します。

```
.s7ecatalogviewer .s7socialshare .s7socialsharepanel
```

**ソーシャル共有パネルの CSS プロパティ**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>パネルの背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 透明色を持つパネルを設定するには、次のように記述します。

```
.s7ecatalogviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

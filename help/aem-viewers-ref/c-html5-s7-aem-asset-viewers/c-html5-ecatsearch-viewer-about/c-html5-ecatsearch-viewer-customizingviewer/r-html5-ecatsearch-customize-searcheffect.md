---
description: ビューアでは、メイン表示に検索結果領域が表示され、カタログ内の語句が強調表示されます。
solution: Experience Manager
title: 検索効果
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 1%

---


# 検索効果{#search-effect}

ビューアでは、メイン表示に検索結果領域が表示され、カタログ内の語句が強調表示されます。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域のCSSプロパティ**

検索結果領域の外観は、以下のCSSクラスセレクターを使用して制御します。

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSSプロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>検索結果領域の背景 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 半透明の黄色の塗りつぶしを使用して検索結果の領域を設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```


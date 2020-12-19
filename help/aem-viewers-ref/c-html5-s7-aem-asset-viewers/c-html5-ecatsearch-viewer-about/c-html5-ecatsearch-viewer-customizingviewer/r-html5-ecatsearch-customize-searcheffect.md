---
description: ビューアでは、メイン表示に検索結果領域が表示され、カタログ内の語句が強調表示されます。
seo-description: ビューアでは、メイン表示に検索結果領域が表示され、カタログ内の語句が強調表示されます。
seo-title: 検索効果
solution: Experience Manager
title: 検索効果
topic: Dynamic media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

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


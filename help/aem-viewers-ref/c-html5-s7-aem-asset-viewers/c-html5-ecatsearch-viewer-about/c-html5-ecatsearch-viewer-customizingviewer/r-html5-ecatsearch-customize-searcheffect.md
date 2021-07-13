---
description: ビューアは、メインビューの検索結果領域を表示して、カタログ内の単語や語句をハイライト表示します。
solution: Experience Manager
title: 検索効果
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# 検索効果{#search-effect}

ビューアは、メインビューの検索結果領域を表示して、カタログ内の単語や語句をハイライト表示します。

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
   <td colname="col1"> <p> <span class="codeph"> 背景  </span> </p> </td> 
   <td colname="col2"> <p>検索結果領域の背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 半透明で黄色の塗りつぶしを使用して検索結果の領域を設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

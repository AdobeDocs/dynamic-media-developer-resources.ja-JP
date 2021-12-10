---
title: 検索効果
description: ビューアは、メインビューに検索結果の領域を表示して、カタログ内の単語や語句をハイライトします。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# 検索効果{#search-effect}

ビューアは、メインビューに検索結果の領域を表示して、カタログ内の単語や語句をハイライトします。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**メインビューア領域の CSS プロパティ**

検索結果領域の外観は、以下の CSS クラスセレクターを使用して制御します。

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS プロパティ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 </span> </p> </td> 
   <td colname="col2"> <p>検索結果領域の背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

例 — 半透明で黄色い塗りつぶしで検索結果の領域を設定するには、次のように記述します。

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

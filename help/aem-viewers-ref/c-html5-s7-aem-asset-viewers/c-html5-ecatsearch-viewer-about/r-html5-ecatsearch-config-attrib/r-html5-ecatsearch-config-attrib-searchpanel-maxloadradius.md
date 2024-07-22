---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c2bbcb99-eeef-4793-a132-d0bd1fefb534
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 5%

---

# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph">-1 に設定すると </span> コンポーネントが初期化されたときやアセットが変更されたときに、すべてのサムネールが同時に読み込まれます。 </p> <p> <span class="codeph"> 0 に設定すると </span> 表示されているサムネールのみが読み込まれます。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> を設定して、表示可能な領域の周りの非表示の行の数を事前に読み込みます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4b7952997f9240e581d21bcdb173f9af}

オプション。

## 初期設定 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## 例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]

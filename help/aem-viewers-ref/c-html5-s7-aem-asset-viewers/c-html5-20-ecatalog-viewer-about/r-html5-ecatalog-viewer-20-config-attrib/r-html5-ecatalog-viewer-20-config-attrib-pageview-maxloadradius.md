---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph">-1 に設定すると </span> コンポーネントはアイドル状態であるときにすべてのカタログフレームをプリロードします。 </p> <p> <span class="codeph"> 0 に設定すると </span> 現在表示されているフレーム、前のフレーム、次のフレームのみがコンポーネントによって読み込まれます。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> を設定して、現在表示されているフレームの周囲の非表示フレームのうち、アイドル状態でプリロードされるフレームの数を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4b7952997f9240e581d21bcdb173f9af}

オプション。

## 初期設定 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`

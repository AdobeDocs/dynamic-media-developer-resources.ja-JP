---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph"> -1</span>に設定すると、コンポーネントはアイドル状態のときにすべてのカタログフレームをプリロードします。 </p> <p> <span class="codeph"> 0</span>に設定すると、コンポーネントは現在表示されているフレーム、前のフレーム、次のフレームのみを読み込みます。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>を設定して、アイドル状態で現在表示されているフレームの周囲にある非表示のフレームの数を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4b7952997f9240e581d21bcdb173f9af}

（オプション）

## 初期設定 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`

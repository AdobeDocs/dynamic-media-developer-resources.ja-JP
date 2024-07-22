---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cf769b2d-be4e-4d93-9620-00a438157693
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph">-1 に設定すると </span> コンポーネントはアイドル状態であるときにすべてのカタログフレームをプリロードします。 </p> <p> <span class="codeph"> 0 に設定すると </span> コンポーネントは表示されているフレーム、前のフレーム、次のフレームのみを読み込みます。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> を設定して、現在表示されているフレームの周囲の非表示フレームのうち、アイドル状態でプリロードされるフレームの数を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4b7952997f9240e581d21bcdb173f9af}

オプション。

## 初期設定 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## 例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]

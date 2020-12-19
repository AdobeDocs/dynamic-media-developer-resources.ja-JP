---
description: 'null'
seo-description: 'null'
seo-title: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic media
uuid: 425624c5-3cbe-4b63-8c6b-eff31f2ed919
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 5%

---


# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph"> -1</span>に設定すると、コンポーネントはアイドル状態のときにすべてのカタログフレームをプリロードします。 </p> <p> <span class="codeph"> 0</span>に設定すると、コンポーネントは現在表示されているフレーム、前のフレーム、次のフレームのみを読み込みます。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>を設定して、現在表示されているフレームの前後の非表示のフレームを、アイドル状態でプリロードする数を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4b7952997f9240e581d21bcdb173f9af}

（オプション）

## 初期設定 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`

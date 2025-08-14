---
title: PageView.fmt
description: PageView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 07aec907-fb9d-41c8-9f32-a4886605db35
source-git-commit: 5432393e265fba888579d700cf2f414dc4f680af
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントが Image Server から画像を読み込むために使用する画像形式を指定します。 指定した形式が – alpha<span class="codeph"> で終わ </span> 場合、コンポーネントは画像を透明コンテンツとしてレンダリングします。 他のすべての画像形式では、コンポーネントは画像を不透明として扱います。 コンポーネントの背景は、デフォルトで白になります。 したがって、透明にするには、<span class="codeph"> background-color</span>CSS プロパティを透明に設定 <span class="codeph"> ます </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-12a6fb2fcbc1476b95bd53ce880dc185}

オプション。

## 初期設定 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## 例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`

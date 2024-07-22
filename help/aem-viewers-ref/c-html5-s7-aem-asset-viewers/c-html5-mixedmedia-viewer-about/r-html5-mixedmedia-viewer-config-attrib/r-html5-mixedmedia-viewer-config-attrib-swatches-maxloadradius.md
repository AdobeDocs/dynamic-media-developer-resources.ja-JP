---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 06f493d7-18c9-4bb1-add6-a0dfd1a689bd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 5%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>コンポーネントのプリロード動作を指定します。 <span class="codeph">-1 に設定すると </span> コンポーネントの初期化時またはアセットの変更時に、すべてのスウォッチが同時に読み込まれます。 </p> <p><span class="codeph"> 0 に設定すると </span> 表示されているスウォッチのみが読み込まれます。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> 可視領域の周囲の非表示の行/列のプリロード数を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`

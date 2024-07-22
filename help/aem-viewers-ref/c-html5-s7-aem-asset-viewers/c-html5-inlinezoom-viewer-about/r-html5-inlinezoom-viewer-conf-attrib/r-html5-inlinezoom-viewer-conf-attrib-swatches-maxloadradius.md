---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 574cb37c-009a-43c7-ae55-8b26c0c096c5
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 5%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> コンポーネントのプリロード動作を指定します。 <span class="codeph">-1 に設定すると </span> コンポーネントが初期化されたときやアセットが変更されたときに、すべてのスウォッチが同時に読み込まれます。 <span class="codeph"> 0 に設定すると </span> 表示されているスウォッチのみが読み込まれます。 </p> <p><span class="codeph"> <span class="varname"> preloadnbr</span></span> は、可視領域の周囲の非表示の行/列のプリロード数を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

オプション。

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`maxloadradius=-1`

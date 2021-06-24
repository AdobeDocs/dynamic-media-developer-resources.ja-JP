---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,Business Practitioner
exl-id: df9d5be4-d1e1-4b72-a7e7-0f3611278d2a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>コンポーネントのプリロード動作を指定します。 <span class="codeph"> -1</span>に設定すると、コンポーネントの初期化時またはアセットの変更時に、すべてのスウォッチが同時に読み込まれます。 </p> <p><span class="codeph"> 0</span>に設定すると、表示されているスウォッチのみが読み込まれます。 </p> <p><span class="codeph"><span class="varname"> </span></span> preloadnbrは、表示されている領域の周りにある非表示の行/列の数を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=-1`

---
description: 'null'
seo-description: 'null'
seo-title: FavoritesView.maxloadradius
solution: Experience Manager
title: FavoritesView.maxloadradius
topic: Dynamic media
uuid: 52347bee-2cdf-4bb4-bb6f-eefff06b82af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---


# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

` [FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph"> -1</span>に設定した場合、コンポーネントの初期化時またはアセットの変更時に、すべてのサムネールが同時に読み込まれます。 </p> <p><span class="codeph"> 0</span>に設定すると、表示されているサムネールのみが読み込まれます。 </p> <p> <span class="codeph"><span class="varname"> preloadnbr</span></span>に設定した場合、表示領域の周囲にある非表示の行をいくつプリロードするかを指定できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`1`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`maxloadradius=0`

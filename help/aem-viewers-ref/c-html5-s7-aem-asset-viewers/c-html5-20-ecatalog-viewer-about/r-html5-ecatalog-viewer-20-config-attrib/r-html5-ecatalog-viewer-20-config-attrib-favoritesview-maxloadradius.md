---
title: FavoritesView.maxloadradius
description: FavoritesView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 6bbf75f1-96e7-496d-9f5c-6f449f76bfdd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

` [FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> コンポーネントのプリロード動作を指定します。 </p> <p>に設定する場合 <span class="codeph"> -1</span>の場合、コンポーネントの初期化時またはアセットの変更時に、すべてのサムネールが同時に読み込まれます。 </p> <p>に設定する場合 <span class="codeph"> 0</span>に設定されている場合、表示されるサムネールのみが読み込まれます。 </p> <p> に設定する場合 <span class="codeph"><span class="varname"> preloadnbr</span></span>を指定すると、表示される領域の周囲に表示されない行を何行プリロードするかを指定できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`1`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`maxloadradius=0`

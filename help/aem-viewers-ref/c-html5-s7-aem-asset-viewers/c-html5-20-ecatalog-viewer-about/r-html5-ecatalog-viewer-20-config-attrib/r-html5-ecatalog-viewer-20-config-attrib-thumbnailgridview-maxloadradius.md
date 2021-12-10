---
title: ThumbnailGridView.maxloadradius
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e93de3b5-b42d-4db8-90b9-9e2aa53af775
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントのプリロード動作を指定します。 </p> <p>に設定する場合 <span class="codeph"> -1</span> コンポーネントの初期化時やアセットの変更時に、サムネールが同時に読み込まれます。 </p> <p>に設定する場合 <span class="codeph"> 0</span> 表示されているサムネールのみが読み込まれます。 </p> <p>設定 <span class="codeph"><span class="varname"> preloadnbr</span></span> は、表示されている領域の周囲にある非表示の行/列のプリロード数を定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-a3abd04c03e14c238a07349ce50d8310}

（オプション）

## 初期設定 {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## 例 {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`

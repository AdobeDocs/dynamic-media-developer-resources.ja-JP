---
description: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,User
exl-id: afc2018f-b222-4fd5-b9dc-88655793efd4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 6%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_2D7F971D503348B8A9559362A1D9B26D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 手順</span></span> </p> </td> 
   <td colname="col2"> <p> 解像度を2倍に増減するために必要なズームインおよびズームアウト操作の回数を設定します。 1回のズーム操作で変化する解像度は、1ステップあたり2^1です。 1回のズーム操作で最大解像度までズームする場合は、 <span class="codeph"> 0</span>に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 制限</span></span> </p> </td> 
   <td colname="col2"> <p> 最大解像度の画像を基準とする最大ズーム解像度を指定します。 初期設定は<span class="codeph"> 1.0</span>で、最大解像度を超えるズームは許可されません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`

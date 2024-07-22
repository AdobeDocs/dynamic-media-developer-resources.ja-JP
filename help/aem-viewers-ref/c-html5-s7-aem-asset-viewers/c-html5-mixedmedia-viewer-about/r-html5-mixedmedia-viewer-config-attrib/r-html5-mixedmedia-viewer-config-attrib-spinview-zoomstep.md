---
title: SpinView.zoomstep
description: SpinView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: afc2018f-b222-4fd5-b9dc-88655793efd4
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_2D7F971D503348B8A9559362A1D9B26D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> ステップ </span></span> </p> </td> 
   <td colname="col2"> <p> 解像度を 2 倍に増減するために必要なズームインおよびズームアウトの回数を設定します。 各ズームアクションの解像度の変化は、1 ステップあたり 2^1 です。 <span class="codeph"> 0</span> に設定すると、1 回のズームアクションで最大解像度にズームできます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 限 </span></span> </p> </td> 
   <td colname="col2"> <p> 最大解像度を指定します。最大解像度は、フル解像度の画像を基準にします。 デフォルトは <span class="codeph"> 1.0</span> で、フル解像度を超えてズームすることはできません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`

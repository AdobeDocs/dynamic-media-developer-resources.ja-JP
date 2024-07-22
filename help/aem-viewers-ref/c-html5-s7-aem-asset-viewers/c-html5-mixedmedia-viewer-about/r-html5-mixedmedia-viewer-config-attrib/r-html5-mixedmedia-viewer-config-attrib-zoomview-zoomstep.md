---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5d978d21-7942-4bd6-b742-9bf4b6fd3ebe
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
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

---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,Business Practitioner
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 必要に応じて、ズームされた画像のプリロードを有効にするには<span class="codeph"> 1</span>に設定し、ズーム画像を増分的に読み込むには<span class="codeph"> 0</span>に設定します。 </p> <p> <p>注意： このオプションを有効にすると、帯域幅の使用量が大幅に増加する可能性があります。 ユーザーがズーム操作を開始していない場合でも、ズームされた画像全体が読み込まれます。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`

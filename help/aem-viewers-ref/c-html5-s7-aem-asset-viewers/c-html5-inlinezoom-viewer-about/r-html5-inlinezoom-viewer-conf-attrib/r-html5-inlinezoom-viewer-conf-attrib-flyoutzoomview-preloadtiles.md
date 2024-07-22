---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 1</span> に設定すると、ズーム画像のプリロードが有効になり、<span class="codeph"> 0</span> に設定すると、必要に応じてズーム画像が増分的に読み込まれます。 </p> <p> <p>メモ：このオプションを有効にすると、帯域幅の使用量が大幅に増加する可能性があります。 ユーザーがズームアクションを開始しない場合でも、ズームされた画像全体が読み込まれます。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

オプション。

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`

---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: 041df5c7-9391-4dde-8988-a83272c7c438
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 1</span>に設定すると、ズームされた画像のプリロードが有効になります。 </p> <p>必要に応じて、 <span class="codeph"> 0</span>に設定して、ズーム画像を増分的に読み込みます。 </p> <p> <p>注意： このオプションを有効にすると、ズーム操作が行われなくても、ズームされた画像全体を読み込む必要があるので、帯域幅使用量が大幅に増加する可能性があることに注意してください。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`

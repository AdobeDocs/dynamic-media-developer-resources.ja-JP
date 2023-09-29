---
title: PanoramicView.fmt
description: コンポーネントで Image Server から画像を読み込む際に使用する画像形式を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

コンポーネントで Image Server から画像を読み込む際に使用する画像形式を指定します。 末尾が「 —alpha」の形式を指定すると、画像が透明にレンダリングされます。 その他のすべての画像形式では、画像は不透明として扱われます。 コンポーネントの背景は、デフォルトで透明です。 したがって、不透明にするには、 `background-color` CSS プロパティをに設定 `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> コンポーネントで Image Server からの画像の読み込みに使用する画像形式を指定します。 末尾が「 —alpha」の形式を指定した場合、コンポーネントは画像を透明なコンテンツとしてレンダリングします。その他のすべての画像形式の場合、コンポーネントは画像を不透明として処理します。 コンポーネントの背景は、デフォルトで透明です。 したがって、不透明にするには、CSS プロパティ background-color を目的の色に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`

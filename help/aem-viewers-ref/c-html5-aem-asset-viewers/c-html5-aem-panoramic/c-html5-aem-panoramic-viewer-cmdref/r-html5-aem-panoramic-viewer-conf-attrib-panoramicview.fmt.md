---
title: PanoramicView.fmt
description: コンポーネントが Image Server から画像を読み込むために使用する画像形式を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

コンポーネントが Image Server から画像を読み込むために使用する画像形式を指定します。 指定した形式が「– alpha」で終わる場合、コンポーネントは画像を透明としてレンダリングします。 その他のすべての画像形式では、コンポーネントは画像を不透明として扱います。 コンポーネントの背景は、デフォルトでは透明になっています。 したがって、不透明にするには、`background-color` CSS プロパティを `desired_color` に設定します

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> コンポーネントが Image Server から画像を読み込むために使用する画像形式を指定します。 指定した形式が「– alpha」で終わる場合、コンポーネントは画像を透明なコンテンツとしてレンダリングします。その他のすべての画像形式では、コンポーネントは画像を不透明として処理します。 コンポーネントの背景は、デフォルトでは透明になっています。 したがって、不透明にするには、背景色 CSS プロパティを目的の色に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`

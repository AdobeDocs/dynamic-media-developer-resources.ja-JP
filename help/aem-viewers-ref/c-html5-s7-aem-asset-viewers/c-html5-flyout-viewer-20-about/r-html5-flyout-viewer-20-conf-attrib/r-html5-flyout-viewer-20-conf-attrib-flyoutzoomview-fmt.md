---
title: FlyoutZoomView.fmt
description: FlyoutZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 4e1ce754-6967-492b-a617-764ee3ec3a55
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントが Image Server から画像を読み込むために使用する画像形式を指定します。 指定した形式が「– alpha」で終わ <span class="codeph"> 場合、コンポーネントは画像を透明コンテンツとしてレンダリング </span> ます。 他のすべての画像形式では、コンポーネントは画像を不透明として扱います。 コンポーネントの背景は、デフォルトで白になります。 したがって、透明にするには、<span class="codeph"> background-color</span>CSS プロパティを透明に設定 <span class="codeph"> ます </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`jpeg`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`fmt=png-alpha`

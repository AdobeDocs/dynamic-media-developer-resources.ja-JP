---
title: FlyoutZoomView.fmt
description: FlyoutZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 6a9a5530-dbde-4090-8545-36bbd7322927
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントで Image Server から画像を読み込む際に使用する画像形式を指定します。 指定した形式が <span class="codeph"> -alpha</span>を指定しない場合、コンポーネントは画像を透明なコンテンツとしてレンダリングします。 その他のすべての画像形式では、画像は不透明として扱われます。 </p> <p>コンポーネントの背景は、デフォルトで白です。 したがって、透明にするには、 <span class="codeph"> background-color</span> CSS プロパティをに設定 <span class="codeph"> 透明</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`

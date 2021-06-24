---
description: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,Business Practitioner
exl-id: 6a9a5530-dbde-4090-8545-36bbd7322927
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントでImage Serverから画像を読み込む際に使用する画像形式を指定します。 末尾が<span class="codeph"> -alpha</span>の形式を指定すると、画像が透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式では、画像は不透明として扱われます。 </p> <p>コンポーネントの背景はデフォルトで白です。 したがって、完全に透明にするには、CSSプロパティ<span class="codeph"> background-color</span>を<span class="codeph"> transparent</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-e6310c8c4e8547689a5b48ceddb3671d}

（オプション）

## 初期設定 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## 例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`

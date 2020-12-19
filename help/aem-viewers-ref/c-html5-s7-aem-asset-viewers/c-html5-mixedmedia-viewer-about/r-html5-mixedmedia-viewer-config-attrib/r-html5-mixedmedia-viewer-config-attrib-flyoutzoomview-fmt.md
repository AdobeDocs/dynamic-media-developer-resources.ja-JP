---
description: コンポーネントでImage Serverからの画像の読み込みに使用する画像形式を指定します。
seo-description: コンポーネントでImage Serverからの画像の読み込みに使用する画像形式を指定します。
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 6f6a69b4-d581-44ff-b089-ce9d0d0170bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

コンポーネントでImage Serverからの画像の読み込みに使用する画像形式を指定します。

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 末尾が<span class="codeph"> -alpha</span>の形式を指定すると、画像が透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式の場合、画像は不透明として扱われます。 </p> <p>コンポーネントの背景色はデフォルトで白です。 したがって、完全に透明にするには、<span class="codeph"> background-color</span> CSSプロパティを<span class="codeph"> transparent</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`

---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,User
exl-id: 07aec907-fb9d-41c8-9f32-a4886605db35
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントがImage Serverから画像を読み込む際に使用する画像形式を指定します。 末尾が<span class="codeph"> -alpha</span>の形式を指定すると、画像が透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式では、画像は不透明として扱われます。 コンポーネントの背景は、デフォルトで白です。 したがって、透明にするには、CSSの<span class="codeph"> background-color</span>プロパティを<span class="codeph"> transparent</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-12a6fb2fcbc1476b95bd53ce880dc185}

（オプション）

## 初期設定 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## 例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`

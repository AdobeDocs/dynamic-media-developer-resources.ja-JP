---
title: PageView.fmt
description: PageView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 07aec907-fb9d-41c8-9f32-a4886605db35
TQID: 'https://experienceleague.adobe.com/f17-tTKGFXLzT-tM62SDIcMOXSK6ksQaJ7guQobq-xc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 4%

---

# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントがImage Serverから画像を読み込むときに使用する画像形式を指定します。 指定された形式が<span class="codeph"> -alpha</span>で終わる場合、コンポーネントは画像を透明コンテンツとしてレンダリングします。 その他のすべての画像形式では、コンポーネントは画像を不透明として扱います。 デフォルトでは、コンポーネントの背景は白です。 したがって、透明にするには、<span class="codeph"> background-color</span> CSS プロパティを<span class="codeph"> transparent</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-12a6fb2fcbc1476b95bd53ce880dc185}

オプション。

## 初期設定 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## 例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`

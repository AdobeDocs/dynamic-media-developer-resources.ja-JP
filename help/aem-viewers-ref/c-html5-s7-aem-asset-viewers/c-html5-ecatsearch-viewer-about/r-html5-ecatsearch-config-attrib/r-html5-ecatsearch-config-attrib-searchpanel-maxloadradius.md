---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c2bbcb99-eeef-4793-a132-d0bd1fefb534
TQID: 'https://experienceleague.adobe.com/h1vgh-2w1mYZXx7MR7korb48n9JuS-pMPFk3HIt4928'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 57
ht-degree: 5%

---

# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph"> -1</span>に設定すると、コンポーネントが初期化されたり、アセットが変更されたりすると、すべてのサムネールが同時に読み込まれます。 </p> <p> <span class="codeph">に設定すると、表示されているサムネールのみが読み込まれます。</span> </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>を設定して、表示領域の周囲にある非表示の行の数がプリロードされるように定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4b7952997f9240e581d21bcdb173f9af}

オプション。

## 初期設定 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## 例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]

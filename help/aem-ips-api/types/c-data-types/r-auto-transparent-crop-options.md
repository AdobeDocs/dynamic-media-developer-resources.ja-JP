---
description: 透明度に基づいて画像を自動的に切り抜く場合に使用するオプションです。
solution: Experience Manager
title: AutoTransparentCropOptions
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 351f63a4-cc1b-4db9-93df-c21acd02e12a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 11%

---

# AutoTransparentCropOptions{#autotransparentcropoptions}

透明度に基づいて画像を自動的に切り抜く場合に使用するオプションです。

構文

## パラメータ {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 許容</span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">透明度に基づいて画像のエッジから空白を削除します。 用途： 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0の場合は色が正確に一致します。 </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1：最も多くの色差を有効にします。 </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

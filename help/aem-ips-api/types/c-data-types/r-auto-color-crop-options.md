---
description: 色に基づいて画像を自動的に切り抜くオプションです。
solution: Experience Manager
title: AutoColorCropOptions
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 9%

---


# AutoColorCropOptions{#autocolorcropoptions}

色に基づいて画像を自動的に切り抜くオプションです。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> corner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 「角を自動切り抜き」の選択 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 耐性</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:重複</span> </td> 
   <td colname="col3">カラーマッチの指定 用途： 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0の場合、色が完全に一致します。 </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1を指定すると、最も多くの色の違いが有効になります。 </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>


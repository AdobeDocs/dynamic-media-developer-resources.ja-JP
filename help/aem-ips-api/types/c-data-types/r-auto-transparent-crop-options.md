---
description: 透明部分に基づいて画像を自動的に切り抜く場合に使用するオプション。
seo-description: 透明部分に基づいて画像を自動的に切り抜く場合に使用するオプション。
seo-title: AutoTransparentCropOptions
solution: Experience Manager
title: AutoTransparentCropOptions
topic: Scene7 Image Production System API
uuid: 4c3d365d-e011-4f38-bea7-68cf0cba7893
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AutoTransparentCropOptions{#autotransparentcropoptions}

透明部分に基づいて画像を自動的に切り抜く場合に使用するオプション。

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
   <td colname="col3">透明度に基づいて画像の境界線から空白を削除します。 用途： 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0を指定すると、色が完全に一致します。 </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1を指定すると、最も多くの色の違いが有効になります。 </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>


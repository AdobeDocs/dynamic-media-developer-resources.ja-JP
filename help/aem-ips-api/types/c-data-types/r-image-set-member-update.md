---
description: このタイプでは、pageReset フィールドは RenderSet と Catalog の画像アセットタイプに対して意味があります。
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

このタイプでは、pageReset フィールドは、RenderSet と Catalog の画像アセットタイプに対して意味があります。

* の場合 `RenderSet`, `pageReset` 新しいレンダリングビュー/スウォッチグループの開始を示します。

* カタログの場合、 `pageReset` は、新しいページビューの開始を示します。 通常、ページビューあたり 2 ページの画像が存在しますが、画像の数は多かれ少なかれ可能です。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 画像セットメンバー配列内のアセットハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">ページをリセットします。 <p>の設定は無視され、の値は強制的に true になります。 <span class="codeph"> 画像セット</span> および <span class="codeph"> スピンセット</span>. </p></td> 
  </tr> 
 </tbody> 
</table>

---
description: このタイプ内の pageReset フィールドは、RenderSet および Catalog 画像アセットタイプにとって意味があります
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

このタイプ内の pageReset フィールドは、RenderSet および Catalog 画像アセットタイプで意味を持ちます。

* `RenderSet` えば、`pageReset` は新しいレンダービュー/スウォッチグループの開始を示します。

* カタログの場合、`pageReset` は新しいページビューの開始を示します。 通常は、ページビューごとに 2 つのページ画像がありますが、件数は増減できます。

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

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
   <td colname="col3">ページをリセットします。 <p><span class="codeph"> ImageSet</span> および <span class="codeph"> SpinSet</span> の設定は無視され、値は true に設定されます。 </p></td> 
  </tr> 
 </tbody> 
</table>

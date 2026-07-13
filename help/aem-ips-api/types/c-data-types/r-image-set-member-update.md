---
description: このタイプ内のpageReset フィールドは、RenderSetおよびカタログ画像アセットタイプに対して意味があります
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
TQID: 'https://experienceleague.adobe.com/c9-ANQJjBlcpQYnSmrD8nQQ08Vllqt3ZcpW6IBJ9-4I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 3%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

このタイプ内のpageReset フィールドは、RenderSetおよびカタログ画像アセットタイプに対して意味があります。

* `RenderSet`の場合、`pageReset`は新しいレンダービュー/スウォッチグループの開始を示します。

* カタログの場合、`pageReset`は新しいページビューの開始を示します。 通常、1つのページビューにつき2つのページ画像がありますが、使用できるページ数は多くても少なくすることもできます。

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
   <td colname="col3"> 画像セットメンバー配列のアセットハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">ページのリセット。 <p>設定は無視され、<span class="codeph"> ImageSet</span>および<span class="codeph"> SpinSet</span>の値はtrueに強制されます。 </p></td> 
  </tr> 
 </tbody> 
</table>


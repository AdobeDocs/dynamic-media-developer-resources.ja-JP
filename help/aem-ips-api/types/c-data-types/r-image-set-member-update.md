---
description: 'このタイプでは、pageResetフィールドは、RenderSetとカタログ画像アセットタイプに対して意味があります '
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API，画像セット
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# ImageSetMemberUpdate{#imagesetmemberupdate}

このタイプでは、pageResetフィールドは、RenderSetとカタログ画像アセットタイプに対して意味があります。

* `RenderSet`の場合、`pageReset`は新しいレンダリングビュー/スウォッチグループの開始を示します。

* カタログの場合、`pageReset`は新しいページビューの開始を示します。 通常、ページビューあたり2ページの画像がありますが、ページビュー数は多い場合と少ない場合があります。

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
   <td colname="col3"> 画像セットのメンバー配列内のアセットハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">ページをリセットします。 <p><span class="codeph"> ImageSet</span>および<span class="codeph"> SpinSet</span>の値は無視され、強制的にtrueになります。 </p></td> 
  </tr> 
 </tbody> 
</table>

---
description: 'このタイプでは、pageResetフィールドは、RenderSetとCatalogの画像アセットタイプに対して有用です '
seo-description: 'このタイプでは、pageResetフィールドは、RenderSetとCatalogの画像アセットタイプに対して有用です '
seo-title: ImageSetMemberUpdate
solution: Experience Manager
title: ImageSetMemberUpdate
topic: Scene7 Image Production System API
uuid: b0226d21-87ba-4e07-9819-79c9df3df13c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

このタイプでは、pageResetフィールドは、RenderSetとCatalogの画像アセットタイプに対して意味を持ちます。

* `RenderSet`の場合、`pageReset`は新しいレンダリング表示/スウォッチグループの開始を示します。

* カタログの場合、`pageReset`は新しいページ表示の開始を示します。 通常、ページ表示あたり2ページの画像がありますが、画像の数は増減できます。

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
   <td colname="col3"> 画像セットメンバ配列内のアセットハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">ページをリセットします。 <p><span class="codeph"> ImageSet</span>および<span class="codeph"> SpinSet</span>の設定は無視され、値が強制的にtrueになります。 </p></td> 
  </tr> 
 </tbody> 
</table>


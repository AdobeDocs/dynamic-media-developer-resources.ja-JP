---
description: setAssetMetadata で使用される特定のアセットのメタデータ値を設定します。 メタデータに加える変更について説明します。
solution: Experience Manager
title: MetadataUpdate
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 99dc1f0c-c4c4-433e-9b91-fa39ef6f84d7
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 1%

---

# [!DNL MetadataUpdate]{#metadataupdate}

setAssetMetadata で使用される特定のアセットのメタデータ値を設定します。 メタデータに加える変更について説明します。

>[!NOTE]
>
>単一の値フィールドが渡されると、アセットのタグ値が指定されたタグ値にリセットされます。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータフィールドハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 値 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータの更新値。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> ブール型メタデータ値（ブール型入力フィールドのみ） </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 長いメタデータ値（整数タイプのフィールドのみ）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> ダブルメタデータ値（float 型フィールドのみ）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 日付メタデータ値（日付型フィールドのみ）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> <p>アセットの既存のタグ値リストに追加します。 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">単一値タグフィールドには、最後の値のみが格納されます。 </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">固定辞書タグフィールドは、値が辞書にない場合はエラーを返します。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3">アセットの既存のタグ値リストを置き換えます。 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">単一値タグフィールドには、最後の値のみが格納されます。 </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">固定辞書タグフィールドは、値が辞書にない場合はエラーを返します。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> 指定された値をアセットのタグ値リストから削除します（存在する場合）。 </td> 
  </tr> 
 </tbody> 
</table>

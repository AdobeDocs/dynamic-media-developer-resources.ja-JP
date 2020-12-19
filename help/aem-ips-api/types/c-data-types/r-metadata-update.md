---
description: setAssetMetadataで使用される特定のアセットのメタデータ値を設定します。 メタデータに対して行う変更について説明します。
seo-description: setAssetMetadataで使用される特定のアセットのメタデータ値を設定します。 メタデータに対して行う変更について説明します。
seo-title: MetadataUpdate
solution: Experience Manager
title: MetadataUpdate
topic: Scene7 Image Production System API
uuid: 09d3940b-117d-4d83-8b12-e86520c9da34
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 1%

---


# MetadataUpdate{#metadataupdate}

setAssetMetadataで使用される特定のアセットのメタデータ値を設定します。 メタデータに対して行う変更について説明します。

>[!NOTE]
>
>単一の値フィールドが渡されると、アセットのタグ値は指定したタグ値にリセットされます。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータフィールドハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータの更新値。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> ブール型メタデータ値（ブール型フィールドのみ） </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 長いメタデータ値（整数型フィールドのみ） </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:重複</span> </td> 
   <td colname="col3"> 重複のメタデータ値（浮動小数点数型のフィールドのみ） </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 日付メタデータ値（日付を入力したフィールドのみ） </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> <p>アセットの既存のタグ値リストに追加します。 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">単一値のタグフィールドには、最後の値のみが格納されます。 </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">値がディクショナリ内にない場合、固定ディクショナリタグフィールドはフォルトを返します。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3">アセットの既存のタグ値リストを置き換えます。 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">単一値のタグフィールドには、最後の値のみが格納されます。 </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">値がディクショナリ内にない場合、固定ディクショナリタグフィールドはフォルトを返します。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> 指定した値が存在する場合は、アセットのタグ値リストーから削除します。 </td> 
  </tr> 
 </tbody> 
</table>


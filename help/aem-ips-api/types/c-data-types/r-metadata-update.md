---
description: setAssetMetadataで使用される特定のアセットのメタデータ値を設定します。 メタデータに加える変更について説明します。
solution: Experience Manager
title: MetadataUpdate
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 99dc1f0c-c4c4-433e-9b91-fa39ef6f84d7
TQID: 'https://experienceleague.adobe.com/55c5TnWcOF5S5XNlWQ1unTzNRKSXH2Fs-JTpvBdXyfo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 1%

---

# [!DNL MetadataUpdate]{#metadataupdate}

setAssetMetadataで使用される特定のアセットのメタデータ値を設定します。 メタデータに加える変更について説明します。

>[!NOTE]
>
>単一の値フィールドを渡すと、アセットのタグ値が指定されたタグ値にリセットされます。

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
   <td colname="col3"> メタデータフィールドハンドル： </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">値</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> メタデータの更新値： </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> ブール型メタデータ値（ブール型フィールドのみ）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 長いメタデータ値（整数型フィールドの場合のみ）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> ダブルメタデータ値（float型フィールドのみ）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 日付メタデータ値（日付入力フィールドのみ）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：StringArray</span> </td> 
   <td colname="col3"> <p>アセットの既存のタグ値リストに追加します。 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">単一値のタグフィールドには、最後の値のみが格納されます。 </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">固定ディクショナリタグフィールドは、値がディクショナリにない場合に障害を返します。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：StringArray</span> </td> 
   <td colname="col3">アセットの既存のタグ値リストを置き換えます。 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">単一値のタグフィールドには、最後の値のみが格納されます。 </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">固定ディクショナリタグフィールドは、値がディクショナリにない場合に障害を返します。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：StringArray</span> </td> 
   <td colname="col3"> アセットのタグ値リストから指定された値を削除します（存在する場合）。 </td> 
  </tr> 
 </tbody> 
</table>

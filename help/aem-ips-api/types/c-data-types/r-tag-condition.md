---
description: タグフィールドの検索条件を定義します。
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
TQID: 'https://experienceleague.adobe.com/5y2KRE0lZvEuY4wZmcJ-ZrKM5bM9OVwMeSdux9iQl6E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 2%

---

# [!DNL TagCondition]{#tagcondition}

タグフィールドの検索条件を定義します。

構文

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
   <td colname="col3"> タグフィールドハンドル： </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">タグフィールドタイプと、値またはvalueArray フィールドが使用されるかどうかに応じて異なります。 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5"><span class="codeph">値</span>が渡された場合、<span class="codeph"> op</span>は文字列定数の一致である必要があります。 条件は、タグ値に関連付けられているアセットと一致します。 </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD"><span class="codeph"> valueArray</span>が渡された場合、op フィールドは、単一または複数値のタグフィールドの定数<span class="codeph"> MatchesAny</span>にすることができます。 <span class="codeph">は<span class="codeph"> valueArray</span>のタグ値の少なくとも1つに関連付けられているすべてのアセットに一致します。はAny</span>条件に一致します。 </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">複数値のタグフィールドの場合、op フィールドは<span class="codeph"> valueArray</span> フィールドを持つ定数<span class="codeph"> MatchesAll</span>に設定できます。 この場合、条件は、<span class="codeph"> valueArray</span>内のすべてのタグ値に関連付けられているアセットにのみ一致します（他のタグ値に加える可能性があります）。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">値</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 一致する値。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：StringArray</span> </td> 
   <td colname="col3"> 複数の一致する値。 </td> 
  </tr> 
 </tbody> 
</table>

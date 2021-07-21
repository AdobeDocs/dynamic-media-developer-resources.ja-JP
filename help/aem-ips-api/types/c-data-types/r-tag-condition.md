---
description: タグフィールドの検索条件を定義します。
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---

# TagCondition{#tagcondition}

タグフィールドの検索条件を定義します。

構文

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
   <td colname="col3"> タグフィールドハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">タグフィールドのタイプと、値またはvalueArrayフィールドのどちらを使用するかによって異なります。 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5"><span class="codeph">値</span>を渡す場合、<span class="codeph"> op</span>は文字列定数Matchesである必要があります。 この条件は、タグ値に関連付けられているアセットと一致します。 </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD"><span class="codeph"> valueArray</span>を渡す場合、opフィールドは、1つの値を持つタグフィールドまたは複数の値を持つタグフィールドの定数<span class="codeph"> MatchesAny</span>を指定できます。 <span class="codeph"> MatchesAny</span>条件は、<span class="codeph"> valueArray</span>内のタグ値の少なくとも1つに関連付けられているアセットと一致します。 </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">複数の値を持つタグフィールドの場合、opフィールドは定数<span class="codeph"> MatchesAll</span>に設定でき、<span class="codeph"> valueArray</span>フィールドを指定します。 この場合、条件は、<span class="codeph"> valueArray</span>（他のタグ値に加えて）すべてのタグ値に関連付けられているアセットのみと一致します。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 一致する値。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 複数の一致する値。 </td> 
  </tr> 
 </tbody> 
</table>

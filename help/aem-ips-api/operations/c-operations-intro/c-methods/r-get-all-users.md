---
description: 配列内のすべてのユーザーを取得します。
solution: Experience Manager
title: getAllUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: db1fd5c9-80f5-463a-870f-be3e38c21bab
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 17%

---

# getAllUsers{#getallusers}

配列内のすべてのユーザーを取得します。

構文

## 許可されているユーザータイプ {#section-68ed5f5fcc5348308dfe074c590caeaa}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-f092ca72f2024d66a1cec690aeab870a}

**入力（getAllUsersParam）**

<table id="table_1FE6DDADBD134E6D8BD4B52F1EAD2E85"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 必須 </th> 
   <th colname="col4" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeInvalid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4">に設定： 
    <ul id="ul_FB9F59A8293B4CCA98E42EBF8412C77B"> 
     <li id="li_3C2E6C4D3478411FA1A34D5CBFFC8108">無効なユーザーを含めるには </span>true を <span class="codeph"> します。 </li> 
     <li id="li_7FCA0DE4BE2248A690076FEC6854F5CE"><span class="codeph"> false</span> 無効なユーザーを省略します。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**出力（getAllUsersReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userArray | `types:UserArray` | はい | すべてのユーザーの配列。 |
| コードフレーズ | `Code Phrase` |  |  |

## 例 {#section-9c9a2d335513478da20652c1b1443731}

このコードサンプルは、すべてのユーザーを返します。 簡潔にするために、応答は切り捨てられます。

**リクエスト**

```java
<ns1:getAllUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getAllUsersParam>
```

**応答**

```java
<ns1:getAllUsersReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userArray>
      <ns1:items>
         <ns1:userHandle>201|agentshadi@hotmail.com</ns1:userHandle>
         <ns1:firstName>333</ns1:firstName>
         <ns1:lastName>333</ns1:lastName>
         <ns1:email>my_email@someaddress.com</ns1:email>
         <ns1:role>TrialSiteUser</ns1:role>
         <ns1:isValid>true</ns1:isValid>
         <ns1:passwordExpires>2006-12-29T04:19:43.039Z</ns1:passwordExpires>
      </ns1:items>
   ...
   </ns1:userArray>
<ns1:getAllUsersReturn>
```

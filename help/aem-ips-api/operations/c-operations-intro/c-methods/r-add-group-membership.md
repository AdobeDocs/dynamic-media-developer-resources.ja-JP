---
description: グループの配列にユーザーを追加します。
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: c5b5e155-d285-4304-98bc-1d938793e2c0
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 12%

---

# addGroupMembership{#addgroupmembership}

グループの配列にユーザーを追加します。

構文

## 許可されたユーザーの種類 {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-e250f6ddb13646808c6a8860b6442bc5}

**入力(addGroupMembershipParam)**

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>必須 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>グループメンバーシップを追加するユーザーに対して処理します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>会社を属するグループに対するハンドルの配列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(addGroupMembershipParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-f7a1f40c3d7a40ea964b29056c734d81}

この例では、`*`groupHandleArray`*`を持つ会社にグループを追加します。 この例では、1つのグループのみを使用します。

**リクエスト**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**応答**

なし

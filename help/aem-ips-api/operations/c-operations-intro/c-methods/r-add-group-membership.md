---
description: ユーザーをグループの配列に追加します。
seo-description: ユーザーをグループの配列に追加します。
seo-title: addGroupMembership
solution: Experience Manager
title: addGroupMembership
topic: Scene7 Image Production System API
uuid: a8e25f27-c300-424d-83ac-e41bb4cb7964
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 11%

---


# addGroupMembership{#addgroupmembership}

ユーザーをグループの配列に追加します。

構文

## 認証済みユーザータイプ{#section-fe950150718a474d8df30d0f4453c022}

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
   <td colname="col4"> <p>グループメンバーシップを追加するユーザーを処理します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>会社の所属先のグループへのハンドルの配列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(addGroupMembershipParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-f7a1f40c3d7a40ea964b29056c734d81}

次の例では、` *`groupHandleArray`*`を持つ会社にグループを追加します。 この例では、1つのグループのみを使用します。

**リクエスト**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**応答**

なし

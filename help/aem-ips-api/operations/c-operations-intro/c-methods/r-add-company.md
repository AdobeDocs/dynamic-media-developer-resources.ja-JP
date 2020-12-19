---
description: 会社をシステムに追加します。
seo-description: 会社をシステムに追加します。
seo-title: addCompany
solution: Experience Manager
title: addCompany
topic: Scene7 Image Production System API
uuid: 2f00a06d-40d1-4ba3-a317-6ea91e25beb3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 9%

---


# addCompany{#addcompany}

会社をシステムに追加します。

システムに追加する会社の名前を送信します。また、会社の有効期限が切れたかどうかを送信することもできます。

この操作を呼び出すと、会社ハンドルと説明フィールドを含む` *`companyInfo`*`型が取得されます。 要求された会社名が既にシステムに存在する場合は、`ipsApiFault`をスローします。

## 認証済みユーザータイプ{#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-c64a21b72585447880760db9e7a12ccb}

**入力(addCompanyParam)**

<table id="table_AA915BAD2E8E4A1B9719725994309CE8"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>追加する会社の名前。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> expires</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:dateTime</span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>会社の有効期限。 このフィールドに対する要求でタイムゾーンを指定します。 タイムゾーンは「中央時間」に調整されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (addCompanyReturn)**

<table id="table_89EBAC0E0FB34793BD843837BB02B518"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>新しい会社の名前、ルートパス、有効期限、および時刻を取り扱います。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-4c8f1bb40d154c77a7b410468206e52b}

この例は、IPSシステムに会社を追加する要求と、他の操作を実行するために必要な追加会社に関する情報の詳細を示す応答を示しています。

**リクエスト**

```java
<ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:addCompanyParam>
```

**応答**

```java
<ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:addCompanyReturn>
```


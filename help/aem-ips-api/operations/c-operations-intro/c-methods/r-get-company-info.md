---
description: 会社ハンドル、会社名、ルートパス、有効期限など、指定した会社に関する情報を返します。 情報を取得するcompanyHandleまたはcompanyNameを指定する必要があります。
seo-description: 会社ハンドル、会社名、ルートパス、有効期限など、指定した会社に関する情報を返します。 情報を取得するcompanyHandleまたはcompanyNameを指定する必要があります。
seo-title: getCompanyInfo
solution: Experience Manager
title: getCompanyInfo
topic: Dynamic Media Image Production System API
uuid: 9218cba8-2873-46b7-90e3-7ab9d5018690
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 6%

---


# getCompanyInfo{#getcompanyinfo}

会社ハンドル、会社名、ルートパス、有効期限など、指定した会社に関する情報を返します。 情報を取得するcompanyHandleまたはcompanyNameを指定する必要があります。

構文

## 認証済みユーザータイプ{#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-7dec8871c89a414c9f066adade1831d8}

**入力(getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> <span class="varname"> companyHandle </span> </span>または<span class="codeph"> <span class="varname"> companyName </span> </span>が必要です。 </p> </td> 
   <td colname="col4"> <p>情報を取得する会社のハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> <span class="varname"> companyHandle </span> </span>または<span class="codeph"> <span class="varname"> companyName </span> </span>が必要です。 </p> </td> 
   <td colname="col4"> <p>情報を取得する会社の名前。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
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
   <td colname="col2"> <p><span class="codeph"> タイプ：会社</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>ハンドルおよび会社に関するその他の説明情報。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

このコードのサンプルを使用すると、会社名とハンドルを使用して、会社に関するすべての情報を返すことができます。 会社の作成時に受け取った応答に類似したデータを返します。

**リクエスト**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**応答**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```


---
description: 指定した会社に関する情報（会社のハンドル、会社名、ルートパス、有効期限など）を返します。 情報を取得するcompanyHandleまたはcompanyNameを指定する必要があります。
seo-description: 指定した会社に関する情報（会社のハンドル、会社名、ルートパス、有効期限など）を返します。 情報を取得するcompanyHandleまたはcompanyNameを指定する必要があります。
seo-title: getCompanyInfo
solution: Experience Manager
title: getCompanyInfo
topic: Scene7 Image Production System API
uuid: 9218cba8-2873-46b7-90e3-7ab9d5018690
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getCompanyInfo{#getcompanyinfo}

指定した会社に関する情報（会社のハンドル、会社名、ルートパス、有効期限など）を返します。 情報を取得するcompanyHandleまたはcompanyNameを指定する必要があります。

構文

## 認証されたユーザータイプ {#section-74f20fb8602e4f96810795bc4b6f7fdf}

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>company <span class="codeph"> Handle <span class="varname"> または</span> NameNameCompany </span> が必 <span class="codeph"><span class="varname"></span></span> 要です。 </p> </td> 
   <td colname="col4"> <p>情報を取得する会社のハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 会社名</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>company <span class="codeph"> Handle <span class="varname"> または</span> NameNameCompany </span> が必 <span class="codeph"><span class="varname"></span></span> 要です。 </p> </td> 
   <td colname="col4"> <p>情報を取得する会社の名前。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getCompanyInfoReturn)**

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> タイプ：会社</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>会社に関するその他の説明情報を処理します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

このコード例は、会社名とハンドルを使用して、会社に関するすべての情報を返します。 会社の作成時に受け取った応答に似たデータを返します。

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


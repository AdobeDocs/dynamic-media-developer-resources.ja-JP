---
description: 会社のジョブログの詳細を取得します。
seo-description: 会社のジョブログの詳細を取得します。
seo-title: getJobLogDetails
solution: Experience Manager
title: getJobLogDetails
topic: Scene7 Image Production System API
uuid: e4314348-2160-4775-a02f-b4892924f064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getJobLogDetails{#getjoblogdetails}

会社のジョブログの詳細を取得します。

応答フィ `logMessage` ールドは、フィールドに基づいてローカライズさ `authHeader` れてい `locale` ます。

## 認証されたユーザータイプ {#section-6f720a7baad64eb3805868c88af9a960}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-47d411a755224c23a4521f10341d66ab}

**入力(getJobLogDetailsParam)**

<table id="table_A77122D73F684B3F8F5AFA1C11C189ED"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ジョブログが属する会社のハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> アクティブまたは完了したジョブのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 元 <span class="varname"> の名</span> 前 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> ジョブログの元の名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 1つ以上のログタイプ定数。 存在する場合は、指定したログタイプのみが返されます。 デフォルトでは、すべてのログタイプが返されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> recordsPerPage <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">返すdetailArray項 <span class="codeph"> 目の</span> 最大数。 最大値とデフォルト値は1000です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">返すPerPage <span class="codeph"></span>-resultsのレコードのページ数。 デフォルト値は 1 です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 並べ <span class="varname"> 替え</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>Job Detail Sort Field定数値（DateまたはLogType）の1つ。 デフォルト値は「日付」です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 並べ替 <span class="varname"> え方向</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>並べ替え方向の文字列定数の1つ。 デフォルト値は昇順です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(getJobLogDetailsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`jobLogArray`*` | `types:JobLogArray` | はい | ジョブログの配列。 |

## 例 {#section-007678b8b8d94e8f91d09f6bc855f394}

このコード例は、特定の会社のジョブログの詳細をすべて返します。 最初のアレイには、標準のジョブログの詳細が含まれます。 埋め込み配列は、ジョブに関する追加情報を返します。

**リクエスト**

```java
<ns1:getJobLogDetailsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:jobHandle>47||Add_2007-09-14-15:04:34</ns1:jobHandle>
</ns1:getJobLogDetailsParam>
```

**応答**

```java
<getJobLogDetailsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>some_address@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
         <detailArray>
            <items>
               <logMessage>Upload has begun!</logMessage>
               <logType>BeginUpload</logType>
            </items>
            <items>
               <logMessage>Add_2007-09-14-15:04:34</logMessage>
               <logType>OriginalJobName</logType>
            </items>
            <items>
               <logMessage>s7oslo</logMessage>
               <logType>JobClient</logType>
            </items>
            ...
         </detailArray>
      </items>
   </jobLogArray>
</getJobLogDetailsReturn>
```


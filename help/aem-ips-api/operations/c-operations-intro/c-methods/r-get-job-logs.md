---
description: 選択した会社の指定されたジョブ ログを取得します。 文字、方向、開始日と終了日、行数で並べ替えることができます。
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
TQID: 'https://experienceleague.adobe.com/lerbQ3ibPCI3zqkrmgPrwTAYp1w6dWxIWYRt2Ij51oA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 9%

---

# getJobLogs{#getjoblogs}

選択した会社の指定されたジョブ ログを取得します。 文字、方向、開始日と終了日、行数で並べ替えることができます。

構文

## 承認済みユーザータイプ {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-8cfdc7994da24678a45edcb37e9a2166}

**入力（getJobLogsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | いいえ | 企業のハンドル。 |
| userHANDLE | `xsd:string` | いいえ | 特定のユーザーによって送信されたジョブのログを取得します。 |
| sortBy | `xsd:string` | いいえ | 並べ替えフィールドを選択できます。 |
| sortDirection | `xsd:string` | いいえ | 並べ替え順序（昇順または降順）。 |
| startDate | `xsd:dateTime` | いいえ | ジョブ・ログの開始日時。 このフィールドのリクエストをタイムゾーンに指定します。 |
| endDate | `xsd:dateTime` | いいえ | ジョブのログが終了した日時。 このフィールドのリクエストをタイムゾーンに指定します。 |
| numRows | `xsd:int` | いいえ | 返される最大行数。 |

**出力（getJobLogsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | はい | ジョブログの配列。 |

## 例 {#section-35871c94b4a44559912577efddbc46a6}

このコードサンプルは、特定の会社のIPS ジョブログを返します。 また、特定のユーザーや企業、ユーザーのジョブログを返すために使用することもできます。

**リクエスト**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**応答**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```

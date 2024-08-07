---
description: 選択した会社の指定したジョブ ログを取得します。 文字、方向、開始日と終了日、行数で並べ替えることができます。
solution: Experience Manager
title: getJobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 9%

---

# getJobLog{#getjoblogs}

選択した会社の指定したジョブ ログを取得します。 文字、方向、開始日と終了日、行数で並べ替えることができます。

構文

## 許可されているユーザータイプ {#section-9df82972265d44c9ad91504a17c3ffa6}

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
| companyHandle | `xsd:string` | いいえ | 会社のハンドル。 |
| userHandle | `xsd:string` | いいえ | 特定のユーザーによって送信されたジョブのログを取得します。 |
| sortBy | `xsd:string` | いいえ | ソートフィールドを選択できます。 |
| sortDirection | `xsd:string` | いいえ | 並べ替え順（昇順または降順）。 |
| startDate | `xsd:dateTime` | いいえ | ジョブ ログが開始された日時。 このフィールドに対するリクエストのタイムゾーンを指定します。 |
| endDate | `xsd:dateTime` | いいえ | ジョブ ログが終了した日時。 このフィールドに対するリクエストのタイムゾーンを指定します。 |
| numRows | `xsd:int` | いいえ | 返される行の最大数。 |

**出力（getJobLogsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | はい | ジョブログの配列。 |

## 例 {#section-35871c94b4a44559912577efddbc46a6}

このコードのサンプルでは、特定の会社の IPS ジョブログを返します。 また、特定のユーザー、会社およびユーザーのジョブログを返すためにも使用できます。

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

---
description: 選択した会社の指定したジョブログを取得します。 文字、方向、開始、終了日、行数で並べ替えることができます。
seo-description: 選択した会社の指定したジョブログを取得します。 文字、方向、開始、終了日、行数で並べ替えることができます。
seo-title: getJobLogs
solution: Experience Manager
title: getJobLogs
uuid: 850ccfad-6cdb-4eda-a20a-762fadadf8b2
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 9%

---


# getJobLogs{#getjoblogs}

選択した会社の指定したジョブログを取得します。 文字、方向、開始、終了日、行数で並べ替えることができます。

構文

## 認証済みユーザータイプ{#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-8cfdc7994da24678a45edcb37e9a2166}

**入力(getJobLogsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | いいえ | 会社ハンドル。 |
| `*`userHandle`*` | `xsd:string` | いいえ | 特定のユーザーが送信したジョブのログを取得します。 |
| `*`sortBy`*` | `xsd:string` | いいえ | フィールドの並べ替えを選択できます。 |
| `*`sortDirection`*` | `xsd:string` | いいえ | 並べ替え順（昇順または降順） |
| `*`startDate`*` | `xsd:dateTime` | いいえ | ジョブログの開始の日時。 このフィールドに対する要求でタイムゾーンを指定します。 |
| `*`endDate`*` | `xsd:dateTime` | いいえ | ジョブログが終了した日時。 このフィールドに対する要求でタイムゾーンを指定します。 |
| `*`numRows`*` | `xsd:int` | いいえ | 返す行の最大数。 |

**出力(getJobLogsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`jobLogArray`*` | `types: JobLogArray` | はい | ジョブログの配列。 |

## 例 {#section-35871c94b4a44559912577efddbc46a6}

このコードのサンプルを使用すると、特定の会社のIPSジョブログを返すことができます。 また、特定のユーザー、会社、ユーザーのジョブログを返す場合にも使用できます。

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


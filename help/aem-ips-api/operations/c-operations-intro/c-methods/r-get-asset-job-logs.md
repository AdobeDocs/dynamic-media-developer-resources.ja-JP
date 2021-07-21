---
description: アセットのジョブログを取得します。 配列に返される項目には、そのアセットのジョブログの各エントリに関する詳細情報が含まれます。 logMessage応答フィールドは、 authHeaderフィールドに基づいてローカライズされます。
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: 88ec5cab-7eb4-48aa-914f-21311593e463
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 9%

---

# getAssetJobLogs{#getassetjoblogs}

アセットのジョブログを取得します。 配列に返される項目には、そのアセットのジョブログの各エントリに関する詳細情報が含まれます。 logMessage応答フィールドは、 authHeaderフィールドに基づいてローカライズされます。

構文

## 許可されたユーザーの種類 {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-9586617e124b4da4acb6b66b2a9adad8}

**入力(getAssetJobLogsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | アセットが属する会社のハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | 取得するジョブログを含むアセットへのハンドル。 |

**出力(getAssetJobLogsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`jobLogArray`*` | `types:AssetJobLogArray` | はい | ジョブログ配列。 |

## 例 {#section-f03d7f3ec5d043d38227f926fb7609f6}

このコードサンプルは、特定のアセットのジョブログを取得します。 応答は、ジョブログ配列と、アセットが使用されたすべてのジョブに関する詳細情報を返します。

**リクエスト**

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**応答**

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```

---
description: 実行するようにスケジュールされたジョブを取得します。
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 21%

---

# getScheduledJobs{#getscheduledjobs}

実行するようにスケジュールされたジョブを取得します。

構文

## 許可されたユーザーの種類 {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-2af604ff8282460990b9237158187f8f}

**入力(getScheduledJobsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社の取っ手。 |
| `*`jobHandle`*` | `xsd:string` | いいえ | ジョブハンドル。 |
| `*`originalName`*` | `xsd:string` | いいえ | `submitJob`で指定された名前。 |

**出力(getScheduledJobsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`jobArray`*` | `types:ScheduledJobArray` | はい | スケジュール済みジョブの配列。 |

## 例 {#section-e79e7da86ba848fd9996aa36de462e6c}

このコード例は、すべてのスケジュール済みジョブをジョブ配列で返します。 配列自体には、ジョブに関する詳細情報が含まれます。

**リクエスト**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**応答**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```

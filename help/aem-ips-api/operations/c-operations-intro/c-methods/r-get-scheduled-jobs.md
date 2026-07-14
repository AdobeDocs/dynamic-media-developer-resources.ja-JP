---
description: 実行するようにスケジュールされたジョブを取得します。
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
TQID: 'https://experienceleague.adobe.com/DNUaAhcCeO8MvLH5YF5-WTA74fCyRKLxvXBKu0ltngk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 18%

---

# getScheduledJobs{#getscheduledjobs}

実行するようにスケジュールされたジョブを取得します。

構文

## 承認済みユーザータイプ {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-2af604ff8282460990b9237158187f8f}

**入力（getScheduledJobsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドルです。 |
| jobHandle | `xsd:string` | いいえ | ジョブハンドル： |
| originalName | `xsd:string` | いいえ | `submitJob`で指定された名前。 |

**出力（getScheduledJobsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| jobArray | `types:ScheduledJobArray` | はい | スケジュールされたジョブの配列。 |

## 例 {#section-e79e7da86ba848fd9996aa36de462e6c}

このコードのサンプルでは、ジョブ配列内のすべてのスケジュール済みジョブを返します。 配列自体には、ジョブに関する詳細情報が含まれています。

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


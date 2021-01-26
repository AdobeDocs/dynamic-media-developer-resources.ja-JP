---
description: 実行するようにスケジュールされたジョブを取得します。
seo-description: 実行するようにスケジュールされたジョブを取得します。
seo-title: getScheduledJobs
solution: Experience Manager
title: getScheduledJobs
topic: Dynamic Media Image Production System API
uuid: 56b0623b-46d7-4d11-8eea-6543ed364b53
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 20%

---


# getScheduledJobs{#getscheduledjobs}

実行するようにスケジュールされたジョブを取得します。

構文

## 認証済みユーザータイプ{#section-bd1835ab508a429f8143b3bdb811d6a4}

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
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`jobHandle`*` | `xsd:string` | いいえ | ジョブハンドル。 |
| `*`originalName`*` | `xsd:string` | いいえ | `submitJob`で指定された名前。 |

**出力(getScheduledJobsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`jobArray`*` | `types:ScheduledJobArray` | はい | スケジュール済みジョブの配列。 |

## 例 {#section-e79e7da86ba848fd9996aa36de462e6c}

このコードのサンプルを使用すると、ジョブ配列内のすべてのスケジュール済みジョブが返されます。 配列自体には、ジョブに関する詳細情報が含まれます。

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


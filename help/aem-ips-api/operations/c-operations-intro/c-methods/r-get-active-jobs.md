---
description: 現在アクティブなジョブをすべて取得します。
seo-description: 現在アクティブなジョブをすべて取得します。
seo-title: getActiveJobs
solution: Experience Manager
title: getActiveJobs
topic: Scene7 Image Production System API
uuid: 3231d349-b254-4dd0-804d-8beaab116b56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getActiveJobs{#getactivejobs}

現在アクティブなジョブをすべて取得します。

構文

## 認証されたユーザータイプ {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**入力(getActiveJobsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | いいえ | 会社の取っ手。 |
| ` *`jobHandle`*` | `xsd:string` | いいえ | ジョブのハンドル。 |
| ` *`originalName`*` | `xsd:string` | いいえ | 元のジョブ名。 |

**出力(getActiveJobsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`jobArray`*` | `xsd:string` | はい | アクティブなジョブの配列。 |

## 例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

このコード例は、IPSで実行している会社のアクティブなジョブをすべて返します。 この場合、IPSスケジューリングコーディネータは、アクティブなジョブが実行されていない状態で無効になっているので、応答は異常です。 通常の状況では、応答は多数のアクティブなジョブを返します。

**リクエスト**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**応答**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```


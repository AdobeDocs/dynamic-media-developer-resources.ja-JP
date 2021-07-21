---
description: 現在アクティブなジョブをすべて取得します。
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 16%

---

# getActiveJobs{#getactivejobs}

現在アクティブなジョブをすべて取得します。

構文

## 許可されたユーザーの種類 {#section-125557a6ea7b4fc894d4bb468cd02118}

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
| `*`companyHandle`*` | `xsd:string` | いいえ | 会社の取っ手。 |
| `*`jobHandle`*` | `xsd:string` | いいえ | ジョブのハンドル。 |
| `*`originalName`*` | `xsd:string` | いいえ | 元のジョブ名。 |

**出力(getActiveJobsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`jobArray`*` | `xsd:string` | はい | アクティブなジョブの配列。 |

## 例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

このコードサンプルは、IPSで実行している会社のアクティブなジョブをすべて返します。 この場合、IPSスケジューリングコーディネータは、アクティブなジョブが実行されていない状態で無効になっているので、応答は通常とは異なります。 通常の状況では、応答は多数のアクティブなジョブを返します。

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

---
description: 現在アクティブなすべてのジョブを取得します。
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
TQID: 'https://experienceleague.adobe.com/YTwzh2h9wVPuURKL5nNFoac2SruwYXDw9oWtd-vzowc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 13%

---

# getActiveJobs{#getactivejobs}

現在アクティブなすべてのジョブを取得します。

構文

## 承認済みユーザータイプ {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**入力（getActiveJobsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | いいえ | 会社のハンドルです。 |
| jobHandle | `xsd:string` | いいえ | ジョブへのハンドル。 |
| originalName | `xsd:string` | いいえ | 元のジョブ名。 |

**出力（getActiveJobsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| jobArray | `xsd:string` | はい | アクティブなジョブの配列。 |

## 例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

このコード サンプルは、IPSで実行されている会社のすべてのアクティブなジョブを返します。 この場合、IPS スケジューリング コーディネーターが無効になっていて、アクティブなジョブが実行されていないため、応答は通常と異なります。 通常の状況では、応答はアクティブなジョブの数を返します。

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


---
description: アクティブなジョブを一時停止します。
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
TQID: 'https://experienceleague.adobe.com/7zMJW9fm8DiAPrO5cCDl87FhFMbgpw5NxoBHmIfEBog'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 14%

---

# pauseJob{#pausejob}

アクティブなジョブを一時停止します。

構文

## 承認済みユーザータイプ {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-7aedb924cf8b4e05a0dc927636d537a0}

**入力（pauseJobParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |
| jobHandle | `xsd:string` | はい | 一時停止するジョブに対応します。 |

**出力（PauseJobReturn）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-ee4914f9496f4bd88556728a48fb22c1}

このコードのサンプルでは、アクティブなジョブを一時停止します。

**リクエスト**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**応答**

なし


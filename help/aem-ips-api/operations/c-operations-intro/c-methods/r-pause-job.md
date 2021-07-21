---
description: アクティブなジョブを一時停止します。
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 18%

---

# pauseJob{#pausejob}

アクティブなジョブを一時停止します。

構文

## 許可されたユーザーの種類 {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-7aedb924cf8b4e05a0dc927636d537a0}

**入力(pauseJobParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社に取り扱う。 |
| `*`jobHandle`*` | `xsd:string` | はい | 一時停止するジョブを処理します。 |

**出力(PauseJobReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-ee4914f9496f4bd88556728a48fb22c1}

このコードサンプルは、アクティブなジョブを一時停止します。

**リクエスト**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**応答**

なし

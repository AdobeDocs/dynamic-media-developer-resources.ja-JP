---
description: 一時停止したジョブを再開します。
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 16%

---

# resumeJob{#resumejob}

一時停止したジョブを再開します。

構文

## 許可されたユーザーの種類 {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**入力(resumeJobParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 再起動するジョブを持つ会社へのハンドル。 |
| `*`jobHandle`*` | `xsd:string` | はい | 一時停止中のジョブへのハンドル。 |

**出力(resumeJobReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-d0524e031f1f43d89430eade19526162}

このコードサンプルを使用すると、一時停止したジョブを再開できます。

**リクエスト**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**応答**

なし

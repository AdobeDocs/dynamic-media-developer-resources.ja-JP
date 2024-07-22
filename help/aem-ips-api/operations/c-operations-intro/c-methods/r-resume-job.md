---
description: 一時停止したジョブを再開します。
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 13%

---

# resumeJob{#resumejob}

一時停止したジョブを再開します。

構文

## 許可されているユーザータイプ {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**入力（resumeJobParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 再起動するジョブを含む会社のハンドル。 |
| jobHandle | `xsd:string` | はい | 一時停止したジョブへのハンドル。 |

**出力（resumeJobReturn）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-d0524e031f1f43d89430eade19526162}

このコード例では、一時停止したジョブを再開します。

**リクエスト**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**応答**

なし

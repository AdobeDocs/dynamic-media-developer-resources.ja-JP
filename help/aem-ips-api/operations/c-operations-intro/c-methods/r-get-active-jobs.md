---
description: 現在アクティブなすべてのジョブを取得します。
solution: Experience Manager
title: getActiveJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 13%

---

# getActiveJob{#getactivejobs}

現在アクティブなすべてのジョブを取得します。

構文

## 許可されているユーザータイプ {#section-125557a6ea7b4fc894d4bb468cd02118}

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
| companyHandle | `xsd:string` | いいえ | 会社へのハンドル。 |
| jobHandle | `xsd:string` | いいえ | ジョブのハンドル。 |
| originalName | `xsd:string` | いいえ | 元のジョブ名。 |

**出力（getActiveJobsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| jobArray | `xsd:string` | はい | アクティブなジョブの配列 |

## 例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

このコードサンプルでは、IPS で実行中の会社のすべてのアクティブなジョブを返します。 この場合、IPS スケジューリングコーディネーターが無効になっており、アクティブなジョブが実行されていないので、応答が異常になります。 通常の状況では、応答は複数のアクティブなジョブを返します。

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

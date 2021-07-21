---
description: 現在のジョブまたはスケジュール済みジョブを削除します。
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 12%

---

# deleteJob{#deletejob}

現在のジョブまたはスケジュール済みジョブを削除します。

構文

## 許可されたユーザーの種類 {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-000c42bc93744b1a8e777f3ec3c272b0}

**入力(deleteJobParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | ジョブが属する会社のハンドル。 |
| `*`jobHandle`*` | `xsd:string` | はい | 削除するジョブのハンドル。 |

**出力**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

このコードサンプルでは、実行中のジョブまたはIPSで実行するようにスケジュールされているジョブを削除します。 別の操作から取得する必要があるジョブハンドルが必要です。

**リクエスト**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**応答**

なし

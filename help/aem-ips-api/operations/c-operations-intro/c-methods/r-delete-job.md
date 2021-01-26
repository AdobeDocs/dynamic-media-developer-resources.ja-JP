---
description: 現在のジョブまたはスケジュール済みのジョブを削除します。
seo-description: 現在のジョブまたはスケジュール済みのジョブを削除します。
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
topic: Dynamic Media Image Production System API
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 12%

---


# deleteJob{#deletejob}

現在のジョブまたはスケジュール済みのジョブを削除します。

構文

## 認証済みユーザータイプ{#section-1b959679dc8147c291126ddf7e061742}

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

**Output**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

このコードサンプルを使用すると、実行中のジョブ、またはIPSで実行するようにスケジュールされているジョブを削除できます。 別の操作から取得する必要があるジョブハンドルが必要です。

**リクエスト**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**応答**

なし

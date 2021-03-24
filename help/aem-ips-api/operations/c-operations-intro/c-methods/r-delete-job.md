---
description: 現在のジョブまたはスケジュール済みのジョブを削除します。
solution: Experience Manager
title: deleteJob
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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

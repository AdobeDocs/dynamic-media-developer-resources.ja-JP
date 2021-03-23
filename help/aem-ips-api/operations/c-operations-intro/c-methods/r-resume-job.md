---
description: 一時停止したジョブを再開します。
seo-description: 一時停止したジョブを再開します。
seo-title: resumeJob
solution: Experience Manager
title: resumeJob
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 15%

---


# resumeJob{#resumejob}

一時停止したジョブを再開します。

構文

## 認証済みユーザータイプ{#section-eab49f4b6d1041179000326a10fee889}

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
| `*`jobHandle`*` | `xsd:string` | はい | 一時停止したジョブへのハンドル。 |

**出力(resumeJobReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-d0524e031f1f43d89430eade19526162}

このコードサンプルを使用すると、一時停止したジョブが再開されます。

**リクエスト**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**応答**

なし

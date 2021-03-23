---
description: アクティブなジョブを一時停止します。
seo-description: アクティブなジョブを一時停止します。
seo-title: pauseJob
solution: Experience Manager
title: pauseJob
uuid: baad2ad6-46f5-4133-a6d9-8ffadf990a06
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 16%

---


# pauseJob{#pausejob}

アクティブなジョブを一時停止します。

構文

## 認証済みユーザータイプ{#section-f2bf306ab4574871bd21f9f7dd681033}

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
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`jobHandle`*` | `xsd:string` | はい | 一時停止するジョブの処理。 |

**出力(PauseJobReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-ee4914f9496f4bd88556728a48fb22c1}

このコードのサンプルを使用すると、アクティブなジョブを一時停止できます。

**リクエスト**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**応答**

なし

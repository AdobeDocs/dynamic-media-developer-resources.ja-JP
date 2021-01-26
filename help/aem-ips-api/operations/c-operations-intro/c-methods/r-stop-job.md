---
description: 進行中のジョブを停止します。
seo-description: 進行中のジョブを停止します。
seo-title: stopJob
solution: Experience Manager
title: stopJob
topic: Dynamic Media Image Production System API
uuid: 698c1652-5afa-4a2c-819a-1ba6ffc6aacf
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 20%

---


# stopJob{#stopjob}

進行中のジョブを停止します。

構文

## 認証済みユーザータイプ{#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-2b64f074e37c4c38849994f3bc65342a}

**入力(stopJobParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| `*`jobHandle`*` | `xsd:string` | はい | 停止するジョブの処理。 |

**出力(stopJobReturn0**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-f7e07fa09ae24dc89685533f20ab3b81}

**リクエスト**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**応答**

なし

---
description: 実行中のジョブを停止します。
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 16%

---

# stopJob{#stopjob}

実行中のジョブを停止します。

構文

## 許可されているユーザータイプ {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-2b64f074e37c4c38849994f3bc65342a}

**入力（stopJobParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社ハンドル。 |
| jobHandle | `xsd:string` | はい | 停止するジョブへのハンドル。 |

**出力（stopJobReturn0**

IPS API は、この操作に対して応答を返しません。

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

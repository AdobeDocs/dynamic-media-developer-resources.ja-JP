---
description: プロジェクトの名前を変更します。
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
TQID: 'https://experienceleague.adobe.com/FjPL1Xn4QAYYCdyeYKA1MiQVay988g-sbuiHpazhcMM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 19%

---

# renameProject{#renameproject}

プロジェクトの名前を変更します。

構文

## 承認済みユーザータイプ {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-43ccd77648784be4a259a723c3e1db40}

**入力（renameProjectParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyName | `xsd:string` | はい | 名前を変更するプロジェクトを持つ会社に処理します。 |
| projectHandle | `xsd:string` | はい | プロジェクトへの取り組み。 |
| projectName | `xsd:string` | はい | 新規プロジェクト名。 |

**出力（renameProjectParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| projectHandle | `xsd:string` | はい | 名前を変更したプロジェクトのハンドル。 |

## 例 {#section-a0a06d9244774795b695a10b92b2a5e7}

このコードのサンプルでは、プロジェクトの名前を変更し、プロジェクト ハンドルを返します。

**リクエスト**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**応答**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```


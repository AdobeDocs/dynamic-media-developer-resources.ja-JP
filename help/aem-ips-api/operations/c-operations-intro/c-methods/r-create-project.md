---
description: 新しいプロジェクトを作成します。
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
TQID: 'https://experienceleague.adobe.com/GKNImvhmX1bOepsV0-6QzgZr5jskJQlaqXCMIT5ue5M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 17%

---

# createProject{#createproject}

新しいプロジェクトを作成します。

構文

## 承認済みユーザータイプ {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-8c741884eb54489bbaad0c444fee80b6}

**入力（createProjectParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 新しいプロジェクトに関連付けられている会社のハンドル。 |
| projectName | `xsd:string` | はい | 新規プロジェクト名。 |

**出力（createProjectParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| projectHandle | `xsd:string` | はい | 新しいプロジェクトへのハンドル。 |

## 例 {#section-a0cd532b67e346d088fbec141231a0e5}

このコード サンプルは、ハンドルで指定された会社に`ApiTestProject`という名前のプロジェクトを作成します。 応答は、プロジェクトにハンドルを返します。

**リクエスト**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```


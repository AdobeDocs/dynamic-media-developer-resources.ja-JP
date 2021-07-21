---
description: 新しいプロジェクトを作成します。
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---

# createProject{#createproject}

新しいプロジェクトを作成します。

構文

## 許可されたユーザーの種類 {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-8c741884eb54489bbaad0c444fee80b6}

**入力(createProjectParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 新しいプロジェクトに関連付けられた会社のハンドル。 |
| `*`projectName`*` | `xsd:string` | はい | 新しいプロジェクト名。 |

**出力(createProjectParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | はい | 新しいプロジェクトのハンドル。 |

## 例 {#section-a0cd532b67e346d088fbec141231a0e5}

このコードサンプルは、ハンドルで指定された会社に`ApiTestProject`という名前のプロジェクトを作成します。 応答は、ハンドルをプロジェクトに返します。

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

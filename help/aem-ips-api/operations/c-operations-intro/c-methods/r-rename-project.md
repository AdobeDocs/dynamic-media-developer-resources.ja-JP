---
description: プロジェクトの名前を変更します。
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 21%

---

# renameProject{#renameproject}

プロジェクトの名前を変更します。

構文

## 許可されたユーザーの種類 {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-43ccd77648784be4a259a723c3e1db40}

**入力(renameProjectParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | はい | 名前を変更するプロジェクトを持つ会社に対して処理します。 |
| `*`projectHandle`*` | `xsd:string` | はい | プロジェクトを処理します。 |
| `*`projectName`*` | `xsd:string` | はい | 新しいプロジェクト名。 |

**出力(renameProjectParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | はい | 名前を変更したプロジェクトのハンドル。 |

## 例 {#section-a0a06d9244774795b695a10b92b2a5e7}

このコード例は、プロジェクトの名前を変更し、プロジェクトハンドルを返します。

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

---
description: 新しいプロジェクトを作成します。
seo-description: 新しいプロジェクトを作成します。
seo-title: createProject
solution: Experience Manager
title: createProject
topic: Scene7 Image Production System API
uuid: e011b7ba-6c15-47ef-9ea1-6189c37e7719
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# createProject{#createproject}

新しいプロジェクトを作成します。

構文

## 認証されたユーザータイプ {#section-17878e2e4c3a44988c9a1af82c2ac319}

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
| ` *`companyHandle`*` | `xsd:string` | はい | 新しいプロジェクトに関連付けられている会社のハンドル。 |
| ` *`projectName`*` | `xsd:string` | はい | 新しいプロジェクト名。 |

**出力(createProjectParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`projectHandle`*` | `xsd:string` | はい | 新しいプロジェクトのハンドル。 |

## 例 {#section-a0cd532b67e346d088fbec141231a0e5}

このコード例では、ハンドルで指定された会社 `ApiTestProject` 内でという名前のプロジェクトを作成します。 応答は、ハンドルをプロジェクトに返します。

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


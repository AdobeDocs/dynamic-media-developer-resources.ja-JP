---
description: 新しいプロジェクトを作成します。
solution: Experience Manager
title: createProject
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 18%

---


# createProject{#createproject}

新しいプロジェクトを作成します。

構文

## 認証済みユーザータイプ{#section-17878e2e4c3a44988c9a1af82c2ac319}

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
| `*`companyHandle`*` | `xsd:string` | はい | 新しいプロジェクトに関連付けられている会社のハンドル。 |
| `*`projectName`*` | `xsd:string` | はい | 新しいプロジェクト名。 |

**出力(createProjectParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | はい | 新しいプロジェクトのハンドル。 |

## 例 {#section-a0cd532b67e346d088fbec141231a0e5}

次のコードのサンプルを使用すると、ハンドルで指定された会社に`ApiTestProject`という名前のプロジェクトが作成されます。 応答がハンドルをプロジェクトに返します。

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


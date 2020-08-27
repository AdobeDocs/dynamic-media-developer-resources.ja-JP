---
description: 新しいパスワードを生成します。
seo-description: 新しいパスワードを生成します。
seo-title: generatePassword
solution: Experience Manager
title: generatePassword
topic: Scene7 Image Production System API
uuid: e3367bfc-d437-4a61-83e8-69830154dc61
translation-type: tm+mt
source-git-commit: 676a020ede1f460aa78e9c34eb3ed37f9e610b17
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 18%

---


# generatePassword{#generatepassword}

新しいパスワードを生成します。

構文

## 認証済みユーザータイプ {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-d516615c906240819a284786efb19863}

**入力(generatePasswordParam)**

なし

**出力(generatePasswordParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`パスワード`*` | `xsd:string` | はい | 新しいパスワードです。 |

## 例 {#section-f580fefdccec46fe95359e3aef0ed17f}

次のコードのサンプルを使用して、パスワードを生成します。 リクエストは、要素や値を含まない単なるパラメーターなので、通常とは異なります。 IPSは、強力なパスワードを返します。

**リクエスト**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**応答**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```


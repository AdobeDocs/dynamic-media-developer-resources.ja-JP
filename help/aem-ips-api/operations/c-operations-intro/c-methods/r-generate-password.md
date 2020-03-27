---
description: 新しいパスワードを生成します。
seo-description: 新しいパスワードを生成します。
seo-title: generatePassword
solution: Experience Manager
title: generatePassword
topic: Scene7 Image Production System API
uuid: e3367bfc-d437-4a61-83e8-69830154dc61
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# generatePassword{#generatepassword}

新しいパスワードを生成します。

構文

## 認証されたユーザータイプ {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
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
| ` *`パスワード`*` | `xsd:string` | はい | 新しいパスワード。 |

## 例 {#section-f580fefdccec46fe95359e3aef0ed17f}

次のコード例では、パスワードを生成します。 リクエストは単にパラメーターであり、囲まれた要素や値は含まれていないので、通常とは異なります。 IPSは堅牢なパスワードを返します。

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


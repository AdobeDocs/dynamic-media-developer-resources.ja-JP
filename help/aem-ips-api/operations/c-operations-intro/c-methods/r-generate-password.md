---
description: 新しいパスワードを生成します。
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 20%

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

**入力 (generatePasswordParam)**

なし

**出力 (generatePasswordParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| パスワード | `xsd:string` | はい | 新しいパスワード。 |

## 例 {#section-f580fefdccec46fe95359e3aef0ed17f}

このコードのサンプルでは、パスワードを生成します。 リクエストは単に要素や値を含まないパラメーターなので、通常とは異なります。 IPS は強力なパスワードを返します。

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

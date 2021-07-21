---
description: 新しいパスワードを生成します。
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 18%

---

# generatePassword{#generatepassword}

新しいパスワードを生成します。

構文

## 許可されたユーザーの種類 {#section-88f7dc11e5c74be281399d8f2e3c9555}

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
| `*`パスワード`*` | `xsd:string` | はい | 新しいパスワード。 |

## 例 {#section-f580fefdccec46fe95359e3aef0ed17f}

このコードサンプルは、パスワードを生成します。 リクエストは、単に要素や値を含まないパラメーターなので、通常と異なります。 IPSは、強力なパスワードを返します。

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

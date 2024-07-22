---
description: getVistaPublishFormats
solution: Experience Manager
title: getVistaPublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 19%

---

# getVistaPublishFormats{#getvignettepublishformats}

構文

## 認証済みユーザータイプ {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**入力（getVignettePublishFormatsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社へのハンドル。 |

**出力（getVignettePublishFormatsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| vignetteFormatArray | `types:VignettePublishFormatArray` | はい | ビネット公開形式の配列。 |

## 例 {#section-2cc32b27cc6243b7b3e273cc05996226}

このコードサンプルは、特定の会社に関連付けられた 2 つのビネット公開形式を返します。 情報は配列で返され、簡潔にするために切り捨てられます。

**リクエスト**

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**応答**

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```

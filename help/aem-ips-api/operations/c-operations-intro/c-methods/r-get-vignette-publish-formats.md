---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
TQID: 'https://experienceleague.adobe.com/2boU6c0m2JZ6kLBXvNVtb0udCXQAP4u8hrFIGk0Pezs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 19%

---

# getVignettePublishFormats{#getvignettepublishformats}

構文

## 承認済みユーザータイプ {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**入力（getVignettePublishFormatsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドルです。 |

**出力（getVignettePublishFormatsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| vignetteFormatArray | `types:VignettePublishFormatArray` | はい | 周辺光量補正パブリッシュ形式の配列。 |

## 例 {#section-2cc32b27cc6243b7b3e273cc05996226}

このコードサンプルは、特定の会社に関連付けられた2つのビネット公開形式を返します。 情報は配列で返され、簡潔にするために切り捨てられます。

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


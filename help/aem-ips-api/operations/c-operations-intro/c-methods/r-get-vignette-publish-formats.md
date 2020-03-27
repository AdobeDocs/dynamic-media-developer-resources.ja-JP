---
description: 'null'
seo-description: 'null'
seo-title: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
topic: Scene7 Image Production System API
uuid: 2cf58002-5c4a-4391-85d4-4a67cb085afa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getVignettePublishFormats{#getvignettepublishformats}

構文

## 認証済みのユーザータイプ {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**入力(getVignettePublishFormatsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の取っ手。 |

**出力(getVignettePublishFormatsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`vignetteFormatArray`*` | `types:VignettePublishFormatArray` | はい | ビネット公開形式の配列です。 |

## 例 {#section-2cc32b27cc6243b7b3e273cc05996226}

このコードサンプルを使用すると、特定の会社に関連付けられた2つのビネット公開形式を返すことができます。 情報は配列で返され、簡潔にするために切り捨てられます。

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


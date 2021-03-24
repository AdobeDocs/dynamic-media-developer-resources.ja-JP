---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 22%

---


# getVignettePublishFormats{#getvignettepublishformats}

構文

## 承認されたユーザータイプ{#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**入力(getVignettePublishFormatsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |

**出力(getVignettePublishFormatsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`vignetteFormatArray`*` | `types:VignettePublishFormatArray` | はい | ビネット公開形式の配列です。 |

## 例 {#section-2cc32b27cc6243b7b3e273cc05996226}

次のコードのサンプルを使用すると、特定の会社に関連付けられた2つのビネット公開形式を返すことができます。 情報は配列で返され、簡潔にするために切り捨てられます。

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


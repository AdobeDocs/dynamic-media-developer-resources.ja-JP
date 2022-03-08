---
description: ビネット公開形式を削除します。
solution: Experience Manager
title: deleteVignetPublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 14%

---

# deleteVignetPublishFormat{#deletevignettepublishformat}

ビネット公開形式を削除します。

## 認証済みユーザータイプ {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-789625ba29df4b5f880914d4c64f77ce}

**入力 (deleteVignetPublishFormatParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | ビネットが属する会社のハンドル。 |
| vignetFormatHandle | `xsd:string` | はい | 削除するビネット公開形式のハンドル。 |

**出力 (deleteVignetPublishFormatParam)**

IPS API はこの操作に対する応答を返しません。

## 例 {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

このコードサンプルは、ハンドルで指定されたビネット公開形式を削除します。

**リクエスト**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**応答**

なし

---
description: 周辺光量補正パブリッシュ形式を削除します。
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
TQID: 'https://experienceleague.adobe.com/e1qIrpGHPuodTx79J1ke-7ULFptiCa6ZoIXyldJvSBY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 10%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

周辺光量補正パブリッシュ形式を削除します。

## 承認済みユーザータイプ {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-789625ba29df4b5f880914d4c64f77ce}

**入力（deleteVignettePublishFormatParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | ビネットが属する会社へのハンドル。 |
| vignetteFormatHandle | `xsd:string` | はい | 削除する周辺光量補正パブリッシュ形式のハンドル。 |

**出力（deleteVignettePublishFormatParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

このコードのサンプルでは、ハンドルで指定された周辺光量補正パブリッシュ形式を削除します。

**リクエスト**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**応答**

なし

---
description: ビネット公開形式を削除します。
seo-description: ビネット公開形式を削除します。
seo-title: deleteVignetPublishFormat
solution: Experience Manager
title: deleteVignetPublishFormat
topic: Scene7 Image Production System API
uuid: 3c8148d5-dec6-4ffa-8ab8-2cd70811ada6
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 13%

---


# deleteVignetPublishFormat{#deletevignettepublishformat}

ビネット公開形式を削除します。

## 認証済みユーザータイプ{#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-789625ba29df4b5f880914d4c64f77ce}

**入力(deleteVignettePublishFormatParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | ビネットが属する会社のハンドル。 |
| ` *`vignetteFormatHandle`*` | `xsd:string` | はい | 削除するビネット公開形式のハンドル。 |

**出力(deleteVignettePublishFormatParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

次のコードサンプルを使用すると、ハンドルで指定されたビネット公開形式を削除できます。

**リクエスト**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**応答**

なし

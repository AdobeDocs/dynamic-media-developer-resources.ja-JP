---
description: アセットの公開ヒストリーを返します。
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 16%

---


# getAssetPublishHistory{#getassetpublishhistory}

アセットの公開ヒストリーを返します。

構文

## 認証済みユーザータイプ{#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-3541bd9914a44b89acfc1d419b560ee6}

**入力(getAssetPublishHistoryParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | アセット公開ヒストリーを含む会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | 調査する公開ヒストリーを持つアセット。 |

**出力(getAssetPublishHistoryReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`pubHistoryArray`*` | `types:PublishHistoryArray` | はい | アセットの公開ヒストリー。 |

## 例 {#section-53897c51e5a047c5bd5ea5a6efb2d114}

このコードのサンプルを使用すると、アセットの公開ヒストリーを返すことができます。 サーバが空の配列を返した場合、アセットは一度も発行されていません。

**リクエスト**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**応答**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```


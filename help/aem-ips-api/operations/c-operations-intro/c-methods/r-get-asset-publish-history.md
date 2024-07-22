---
description: アセットの公開履歴を返します。
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 14%

---

# getAssetPublishHistory{#getassetpublishhistory}

アセットの公開履歴を返します。

構文

## 許可されているユーザータイプ {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-3541bd9914a44b89acfc1d419b560ee6}

**入力（getAssetPublishHistoryParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | アセット公開履歴を含む会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | 公開履歴を調査するアセット。 |

**出力（getAssetPublishHistoryReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| pubHistoryArray | `types:PublishHistoryArray` | はい | アセットの公開履歴。 |

## 例 {#section-53897c51e5a047c5bd5ea5a6efb2d114}

このコードサンプルでは、アセットの公開履歴を返します。 サーバーが空の配列を返した場合、アセットが公開されたことはありません。

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

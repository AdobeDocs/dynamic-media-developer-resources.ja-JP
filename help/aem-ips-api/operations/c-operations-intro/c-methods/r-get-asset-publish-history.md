---
description: アセットの公開履歴を返します。
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
TQID: 'https://experienceleague.adobe.com/fXYa2SsttVpR9a1bebJ1oouyK8peSZ5GdgldPqU9s1g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 14%

---

# getAssetPublishHistory{#getassetpublishhistory}

アセットの公開履歴を返します。

構文

## 承認済みユーザータイプ {#section-3b9d6a129093458fa8890139a2718912}

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
| companyHandle | `xsd:string` | はい | アセットの公開履歴を持つ会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | 確認したい公開履歴が含まれているアセット。 |

**出力（getAssetPublishHistoryReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| pubHistoryArray | `types:PublishHistoryArray` | はい | アセットの公開履歴。 |

## 例 {#section-53897c51e5a047c5bd5ea5a6efb2d114}

このコードサンプルは、アセットの公開履歴を返します。 サーバーが空の配列を返した場合、アセットが公開されたことはありません。

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


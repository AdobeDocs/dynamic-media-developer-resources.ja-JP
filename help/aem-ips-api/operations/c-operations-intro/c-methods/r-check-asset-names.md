---
description: 会社の画像サービング/画像レンダリング カタログ名前空間のすべての名前に対してアセット名を比較して、IPS IDの競合をチェックします。
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
TQID: 'https://experienceleague.adobe.com/RbFXhRqcaGXLMAeJhXMzho-ylSe2ktcKwvdbFtrcppM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 11%

---

# checkAssetNames{#checkassetnames}

会社の画像サービング/画像レンダリング カタログ名前空間のすべての名前に対してアセット名を比較して、IPS IDの競合をチェックします。

構文

## 承認済みユーザータイプ {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## パラメーター {#section-9c75b00f2072453abea0bdefc6ad7c99}

**入力（checkAssetNamesParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | いいえ | ユーザーを含む会社へのハンドル。 |
| assetNamesArray | `types:StringArray` | はい | チェックするアセット名の配列。 |

**出力（checkAssetNamesReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | はい | 使用中のアセット名の配列。 |

## 例 {#section-bc5d120d74614a63a425ca3acc337219}

このサンプルコードでは、指定した会社で使用されているアセット名をリクエストします。 応答は、使用中のアセット名の配列を返します。

**リクエスト**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**応答**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```


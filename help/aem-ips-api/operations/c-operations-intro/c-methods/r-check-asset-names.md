---
description: アセット名と会社の画像サービング/画像レンダリングカタログ名前空間のすべての名前を比較することで、IPS ID の競合をチェックします。
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 12%

---

# checkAssetNames{#checkassetnames}

アセット名と会社の画像サービング/画像レンダリングカタログ名前空間のすべての名前を比較することで、IPS ID の競合をチェックします。

構文

## 認証済みユーザータイプ {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## パラメーター {#section-9c75b00f2072453abea0bdefc6ad7c99}

**入力 (checkAssetNamesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | いいえ | ユーザーを含む会社へのハンドル。 |
| assetNamesArray | `types:StringArray` | はい | 確認するアセット名の配列。 |

**出力 (checkAssetNamesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | はい | 使用中のアセット名の配列。 |

## 例 {#section-bc5d120d74614a63a425ca3acc337219}

このサンプルコードは、指定した会社で使用中のアセット名をリクエストします。 応答は、使用中のアセット名の配列を返します。

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

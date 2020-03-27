---
description: アセット名と会社の画像サービング/画像レンダリングカタログ名前空間のすべての名前を比較して、IPS IDの競合を確認します。
seo-description: アセット名と会社の画像サービング/画像レンダリングカタログ名前空間のすべての名前を比較して、IPS IDの競合を確認します。
seo-title: checkAssetNames
solution: Experience Manager
title: checkAssetNames
topic: Scene7 Image Production System API
uuid: 91d073a8-7648-429b-aa5c-c7d595550299
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# checkAssetNames{#checkassetnames}

アセット名と会社の画像サービング/画像レンダリングカタログ名前空間のすべての名前を比較して、IPS IDの競合を確認します。

構文

## 認証されたユーザータイプ {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## パラメータ {#section-9c75b00f2072453abea0bdefc6ad7c99}

**入力(checkAssetNamesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | いいえ | ユーザーを含む会社のハンドル。 |
| ` *`assetNamesArray`*` | `types:StringArray` | はい | 確認するアセット名の配列。 |

**出力(checkAssetNamesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`inUseNameArray`*` | `types:StringArray` | はい | 使用中のアセット名の配列。 |

## 例 {#section-bc5d120d74614a63a425ca3acc337219}

このサンプルコードは、指定した会社で使用されているアセット名を要求します。 応答は、使用中のアセット名の配列を返します。

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


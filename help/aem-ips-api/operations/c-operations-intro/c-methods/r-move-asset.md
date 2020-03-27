---
description: アセットを特定のフォルダに移動します。
seo-description: アセットを特定のフォルダに移動します。
seo-title: moveAsset
solution: Experience Manager
title: moveAsset
topic: Scene7 Image Production System API
uuid: cabeb7b7-ab0b-44d0-ad90-623f76e4323d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveAsset{#moveasset}

アセットを特定のフォルダに移動します。

構文

## 認証されたユーザータイプ {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-dd0bbdf293aa4563af70a91f97c861f1}

**Input (moveAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の取り扱い。 |
| ` *`assetHandle`*` | `xsd:string` | はい | 移動するアセットの処理。 |
| ` *`folderHandle`*` | `xsd:string` | はい | 宛先フォルダーへのハンドル。 |

**出力(moveAssetReturn)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-78333769f4f14e2886fdf06433c9d2ad}

このコードサンプルを使用すると、アセットをフォルダに移動できます。

**リクエスト**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**応答**

なし

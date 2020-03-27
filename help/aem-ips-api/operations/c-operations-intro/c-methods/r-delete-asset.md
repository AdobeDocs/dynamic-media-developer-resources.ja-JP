---
description: アセットを削除します。
seo-description: アセットを削除します。
seo-title: deleteAsset
solution: Experience Manager
title: deleteAsset
topic: Scene7 Image Production System API
uuid: 47f700e0-04bf-4d33-a18a-d938f7e9e326
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteAsset{#deleteasset}

アセットを削除します。

構文

## 認証されたユーザータイプ {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、アセットに対する読み取りおよび削除のアクセス権を持っている必要があります。

## パラメータ {#section-0eed164e278b456fbdfb7a50727a0416}

**入力(deleteAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | フォルダーが属する会社のハンドル。 |
| ` *`assetHandle`*` | `xsd:string` | はい | 削除するアセットのハンドル。 |

**出力(deleteAssetParam)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-d5657289f5234bb0a613dcf691507958}

このサンプルコードは、特定の会社から任意の種類のアセットを削除します。 別の操作から取得する必要があるアセットハンドルが必要です。

**リクエスト**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**応答**

なし

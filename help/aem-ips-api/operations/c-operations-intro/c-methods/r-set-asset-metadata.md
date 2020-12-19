---
description: アセットのメタデータ値を設定します。 メタデータの更新の配列を処理して、値をバッチで設定します。
seo-description: アセットのメタデータ値を設定します。 メタデータの更新の配列を処理して、値をバッチで設定します。
seo-title: setAssetMetadata
solution: Experience Manager
title: setAssetMetadata
topic: Scene7 Image Production System API
uuid: 17fe8277-a164-4f91-af96-ea43d41bd4f2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 9%

---


# setAssetMetadata{#setassetmetadata}

アセットのメタデータ値を設定します。 メタデータの更新の配列を処理して、値をバッチで設定します。

構文

## 認証済みユーザータイプ{#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、アセットに対する読み取りアクセス権を持っている必要があります。

## パラメータ {#section-bcdcff30905e444388811e897b2824bd}

**入力(setAssetMetadataParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 更新するアセットを含む会社へのハンドル。 |
| ` *`assetHandle`*` | `xsd:string` | はい | アセットのハンドル。 |
| ` *`updateArray`*` | `types:MetadataUpdateArray` | はい | メタデータ更新配列の更新。 |

**出力(setAssetMetadataReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-1ab412e7ee1d4d6d8469b0b403598c42}

このコードのサンプルでは、メタデータの更新の配列を使用して、指定したアセットのメタデータを設定します。

**リクエスト**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**応答**

なし

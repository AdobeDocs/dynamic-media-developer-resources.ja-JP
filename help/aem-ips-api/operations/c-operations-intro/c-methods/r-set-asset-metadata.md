---
description: アセットのメタデータ値を設定します。 メタデータ更新の配列を操作して、値をバッチで設定します。
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 8%

---

# setAssetMetadata{#setassetmetadata}

アセットのメタデータ値を設定します。 メタデータ更新の配列を操作して、値をバッチで設定します。

構文

## 許可されているユーザータイプ {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、アセットへの読み取りアクセス権が必要です。

## パラメーター {#section-bcdcff30905e444388811e897b2824bd}

**入力（setAssetMetadataParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 更新するアセットを持つ会社のハンドル。 |
| assetHandle | `xsd:string` | はい | アセットへのハンドル。 |
| updateArray | `types:MetadataUpdateArray` | はい | メタデータ更新配列の更新。 |

**出力（setAssetMetadataReturn）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-1ab412e7ee1d4d6d8469b0b403598c42}

このコードサンプルでは、メタデータ更新の配列を使用して、指定したアセットのメタデータを設定します。

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

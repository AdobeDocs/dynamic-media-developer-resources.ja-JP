---
description: アセットのメタデータ値を設定します。 メタデータ更新の配列を使用して、値をバッチで設定できます。
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
TQID: 'https://experienceleague.adobe.com/b8E8BK8pyJQiYlR2yNMbYPWcLVNfmAvI5WaOBuaBz1E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 8%

---

# setAssetMetadata{#setassetmetadata}

アセットのメタデータ値を設定します。 メタデータ更新の配列を使用して、値をバッチで設定できます。

構文

## 承認済みユーザータイプ {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーはアセットへの読み取りアクセス権を持っている必要があります。

## パラメーター {#section-bcdcff30905e444388811e897b2824bd}

**入力（setAssetMetadataParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 更新するアセットを持つ会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | アセットのハンドルです。 |
| updateArray | `types:MetadataUpdateArray` | はい | メタデータの更新配列を更新します。 |

**出力（setAssetMetadataReturn）**

IPS APIは、この操作に対する応答を返しません。

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


---
description: 会社のアセットの元のファイルパスを取得します。
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
TQID: 'https://experienceleague.adobe.com/D8lKzaqYSHdG-CXVAmlv5cuAuuEXEWlFSnqpiX8RkFI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 13%

---

# getOriginalFilePaths{#getoriginalfilepaths}

会社のアセットの元のファイルパスを取得します。

構文

## 承認済みユーザータイプ {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>アセットへの読み取りアクセスが必要です。

## パラメーター {#section-a6b394daba6e49a8882cf3051035d9d1}

**入力（getOriginalFilePathsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドルです。 |
| assetHandleArray | `types:HandleArray` | はい | 元のファイルパスを取得するアセットへのハンドルの配列。 |

**出力（getOriginalFilePathsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| originalFileArray | `types:StringArray` | はい | 元のファイルパスを表す文字列の配列。 |

## 例 {#section-a966e783a2ba49f5b6b0f961329ab2f8}

このコードサンプルは、アセットハンドル配列内の一意のアセットハンドルで指定されたアセットのファイルパスを返します。

**リクエスト**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**応答**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```

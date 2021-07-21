---
description: 会社のアセットの元のファイルパスを取得します。
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 15%

---

# getOriginalFilePaths{#getoriginalfilepaths}

会社のアセットの元のファイルパスを取得します。

構文

## 許可されたユーザーの種類 {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>アセットへの読み取りアクセス権が必要です。

## パラメータ {#section-a6b394daba6e49a8882cf3051035d9d1}

**入力(getOriginalFilePathsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社の取っ手。 |
| `*`assetHandleArray`*` | `types:HandleArray` | はい | 元のファイルパスを取得するアセットに対するハンドルの配列。 |

**出力(getOriginalFilePathsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`originalFileArray`*` | `types:StringArray` | はい | 元のファイルパスを表す文字列の配列。 |

## 例 {#section-a966e783a2ba49f5b6b0f961329ab2f8}

このコードサンプルは、一意のアセットハンドルを持つアセットのファイルパスをアセットハンドル配列で返します。

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

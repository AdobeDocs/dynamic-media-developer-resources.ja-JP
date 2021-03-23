---
description: 会社のアセットの元のファイルパスを取得します。
seo-description: 会社のアセットの元のファイルパスを取得します。
seo-title: getOriginalFilePaths
solution: Experience Manager
title: getOriginalFilePaths
uuid: c4acf288-1a57-4295-806b-348f15a089cc
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 13%

---


# getOriginalFilePaths{#getoriginalfilepaths}

会社のアセットの元のファイルパスを取得します。

構文

## 認証済みユーザータイプ{#section-da8d8561e9174e938f3595a5d6e50089}

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
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`assetHandleArray`*` | `types:HandleArray` | はい | 元のファイルパスを取得するアセットへのハンドルの配列。 |

**出力(getOriginalFilePathsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`originalFileArray`*` | `types:StringArray` | はい | 元のファイルパスを表す文字列の配列です。 |

## 例 {#section-a966e783a2ba49f5b6b0f961329ab2f8}

このコードのサンプルを使用すると、アセットハンドル配列内の一意のアセットハンドルで指定されたアセットのファイルパスを返すことができます。

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


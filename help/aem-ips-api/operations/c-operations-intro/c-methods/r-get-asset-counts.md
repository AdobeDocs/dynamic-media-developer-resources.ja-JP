---
description: 特定の会社に関連付けられているアセットとアセットの数を取得します。
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
TQID: 'https://experienceleague.adobe.com/gvFs-dqQ8oR38MTKrEYaap31BH-MtSaRtGtJd5FO-MY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 8%

---

# getAssetCounts{#getassetcounts}

特定の会社に関連付けられているアセットとアセットの数を取得します。

返される`countArray`は`assetTypes` （データ型`xsd:string`）の配列で構成され、それぞれに独自のカウント フィールド （データ型`xsd:int`）が含まれており、配列の要素ごとに複数のアセットタイプを表すことができます。構文

## 承認済みユーザータイプ {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**入力（getAssetCountsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | カウントするアセットを持つ会社へのハンドル。 |

**出力（getAssetCountsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| countArray | `types:AssetCountArray` | いいえ | 配列の要素ごとに複数のアセットタイプを表すことができる、各アセットタイプに独自のカウントフィールドを持つ配列。 |

## 例 {#section-6052a503eb3843f6adb99e200fdba280}

このコード サンプルでは、IPS Web サービス サーバーに送信された`getAssetCountsParam`のフィールドとして会社のハンドルを使用して、アセット数を取得します。

**リクエスト**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**応答**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```


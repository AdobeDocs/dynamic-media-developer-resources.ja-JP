---
description: 特定の会社に関連付けられているアセットとアセット数を取得します。
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 10%

---

# getAssetCounts{#getassetcounts}

特定の会社に関連付けられているアセットとアセット数を取得します。

この `countArray` 返されるは、 `assetTypes` ( データタイプ `xsd:string`)、それぞれに独自のカウントフィールド ( データタイプ `xsd:int`) を使用して、配列の要素ごとに複数のアセットタイプを表現できます。
構文

## 認証済みユーザータイプ {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**入力 (getAssetCountsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | カウントするアセットを含む会社へのハンドル。 |

**出力 (getAssetCountsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| countArray | `types:AssetCountArray` | いいえ | アセットタイプの配列で、それぞれに独自のカウントフィールドがあり、配列の要素ごとに複数のアセットタイプを表現できます。 |

## 例 {#section-6052a503eb3843f6adb99e200fdba280}

このコードサンプルでは、会社のハンドルを `getAssetCountsParam` アセット数を取得するために IPS Web サービスサーバに送信されました。

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

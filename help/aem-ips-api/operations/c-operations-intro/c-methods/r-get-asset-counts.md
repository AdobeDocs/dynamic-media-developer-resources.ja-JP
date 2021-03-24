---
description: 特定の会社に関連付けられているアセットとアセット数を取得します。
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Mediaクラシック，SDK/API，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 10%

---


# getAssetCounts{#getassetcounts}

特定の会社に関連付けられているアセットとアセット数を取得します。

返される`countArray`は、`assetTypes` （データ型`xsd:string`）の配列で構成され、それぞれに独自のカウントフィールド（データ型`xsd:int`）があり、配列の要素ごとに複数のアセット型を表現できます。
構文

## 認証済みユーザータイプ{#section-6234754722184e828352f10eb18fbce9}

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

**入力(getAssetCountsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | カウントするアセットを含む会社へのハンドル。 |

**出力(getAssetCountsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | いいえ | アセットタイプの配列。それぞれに独自のカウントフィールドがあり、配列の要素ごとに複数のアセットタイプを表現できます。 |

## 例 {#section-6052a503eb3843f6adb99e200fdba280}

このコードのサンプルでは、会社のハンドルをIPS Webサービスサーバに送信される`getAssetCountsParam`のフィールドとして使用し、アセット数を取得します。

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


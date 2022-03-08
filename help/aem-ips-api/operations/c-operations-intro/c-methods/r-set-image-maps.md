---
description: アセットの画像マップを設定します。
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 11%

---

# setImageMaps{#setimagemaps}

アセットの画像マップを設定します。

既に画像マップを作成している必要があります。 画像マップは、配列から検索される順に適用されます。 つまり、2 つ目の画像マップは最初の画像マップをオーバーレイし、3 つ目の画像マップは 2 つ目の画像マップをオーバーレイし、以下同様に続きます。

## 認証済みユーザータイプ {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-2292ec1aead947ef8741dd0653a41f42}

**入力 (setImageMapsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社の取り扱い。 |
| assetHandle | `xsd:string` | はい | アセットハンドル。 |
| imageMapArray | `types:ImageMapDefinitionArray` | はい | 定義済み画像マップの配列。 |

**出力 (setImageMapsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | はい | アセットに適用された画像マップハンドルを持つ配列。 |

## 例 {#section-fe2e35662a6a4ee29cf250c9fd180371}

このコードサンプルは、画像アセットの 2 つの画像マップを設定します。 このコードは、画像マップが呼び出されたときの形状の種類、領域、および操作を指定します。 応答には、画像マップに対するハンドルを持つ配列が含まれます。

**リクエスト**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```

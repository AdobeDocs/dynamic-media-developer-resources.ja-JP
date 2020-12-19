---
description: アセットの画像マップを設定します。
seo-description: アセットの画像マップを設定します。
seo-title: setImageMaps
solution: Experience Manager
title: setImageMaps
topic: Scene7 Image Production System API
uuid: 1dd7e032-34b4-464d-8ec6-7ad282d12891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 10%

---


# setImageMaps{#setimagemaps}

アセットの画像マップを設定します。

既に画像マップを作成しておく必要があります。 画像マップは、アレイから検索された順に適用される。 つまり、2番目の画像マップは1番目の画像をオーバーレイし、3番目の画像マップは2番目の画像をオーバーレイし、以下同様に重ねて表示されます。

## 認証済みユーザータイプ{#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-2292ec1aead947ef8741dd0653a41f42}

**入力(setImageMapsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| ` *`assetHandle`*` | `xsd:string` | はい | アセットハンドル |
| ` *`imageMapArray`*` | `types:ImageMapDefinitionArray` | はい | 定義済みの画像マップの配列。 |

**出力(setImageMapsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`imageMapHandleArray`*` | `types:HandleArray` | はい | アセットに適用される画像マップハンドルを持つ配列。 |

## 例 {#section-fe2e35662a6a4ee29cf250c9fd180371}

このコードのサンプルでは、1つの画像アセットに対して2つの画像マップを設定します。 このコードは、画像マップを呼び出す際に実行される形状の種類、領域、およびアクションを指定します。 応答には、画像マップに対するハンドルを持つ配列が含まれます。

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


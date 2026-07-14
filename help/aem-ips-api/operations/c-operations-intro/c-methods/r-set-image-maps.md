---
description: アセットの画像マップを設定します。
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
TQID: 'https://experienceleague.adobe.com/sOGDO0ruTEK1DS5Sc-4nhLfViddEKCLDLJlpC-8H3g0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 9%

---

# setImageMaps{#setimagemaps}

アセットの画像マップを設定します。

画像マップは作成済みである必要があります。 画像マップは、配列から取得する順序で適用されます。 これは、2番目の画像マップが1番目の画像をオーバーレイし、3番目の画像が2番目の画像をオーバーレイすることを意味します。

## 承認済みユーザータイプ {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-2292ec1aead947ef8741dd0653a41f42}

**入力（setImageMapsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドル。 |
| assetHandle | `xsd:string` | はい | アセットのハンドル： |
| imageMapArray | `types:ImageMapDefinitionArray` | はい | 定義済みの画像マップの配列。 |

**出力（setImageMapsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | はい | 画像マップハンドルがアセットに適用された配列。 |

## 例 {#section-fe2e35662a6a4ee29cf250c9fd180371}

このコードサンプルでは、画像アセットに2つの画像マップを設定します。 このコードは、画像マップの呼び出し時に実行されるシェイプタイプ、領域、およびアクションを指定します。 応答には、画像マップへのハンドルを含む配列が含まれます。

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


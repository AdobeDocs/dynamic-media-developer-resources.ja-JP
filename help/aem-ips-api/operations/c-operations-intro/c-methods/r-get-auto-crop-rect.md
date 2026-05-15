---
description: 背景色または透明度に基づいて、画像の切り抜き領域を返します。
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
TQID: 'https://experienceleague.adobe.com/cDQ-P-vZGfOyPASRMfemIKnphk5GavTU85m4vJq83bc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 152
ht-degree: 13%

---

# getAutoCropRect{#getautocroprect}

背景色または透明度に基づいて、画像の切り抜き領域を返します。

構文

## 承認済みユーザータイプ {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**入力（getAutoCropRectParam）**

>[!NOTE]
>
>このメソッドを呼び出す際に、autoColorCropOptionsまたはautoTransparentCropOptionsのいずれかを指定します。

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 取り扱うアセットを持つ会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | 操作するアセットへのハンドル。 |
| autoColorCropOptions | `types:AutoColorCropOptions` | いいえ | カラーに基づいてクロップ長方形を計算します。 [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)を参照してください。 |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | いいえ | 透明に基づいて切り抜き長方形を計算します。 [自動透明クロップオプション ](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)を参照してください。 |

**出力（getAutoCropRectReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| xOffset | `xsd:int` | はい | 計算された切り抜き領域の左ピクセルの開始座標。 |
| yOffset | `xsd:int` | はい | 計算された切り抜き領域の先頭ピクセル座標。 |
| 幅 | `xsd:int` | はい | 計算されたトリミング領域の幅（ピクセル単位）。 |
| 高さ | `xsd:int` | はい | 計算されたトリミング領域の高さ（ピクセル単位）。 |

## 例 {#section-ba65bd66086d491cad1cea535954ee1f}

**リクエスト**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**応答**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

---
description: 背景色または透明度に基づいて、画像の切り抜き領域を返します。
solution: Experience Manager
title: getAutoCropDirect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 13%

---

# getAutoCropDirect{#getautocroprect}

背景色または透明度に基づいて、画像の切り抜き領域を返します。

構文

## 許可されているユーザータイプ {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

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
>このメソッドを呼び出す場合は、autoColorCropOptions または autoTransparentCropOptions を指定します。

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 操作するアセットを持つ会社のハンドル。 |
| assetHandle | `xsd:string` | はい | 操作するアセットへのハンドル。 |
| autoColorCropOptions | `types:AutoColorCropOptions` | いいえ | カラーに基づいてトリミング長方形を計算します。 [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6) を参照してください。 |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | いいえ | 透明度に基づいてトリミング長方形を計算します。 [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b) を参照。 |

**出力（getAutoCropRectReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| xOffset | `xsd:int` | はい | 計算された切り抜き領域の左ピクセル開始座標。 |
| yOffset | `xsd:int` | はい | 計算された切り抜き領域の開始トップピクセル座標。 |
| 幅 | `xsd:int` | はい | 計算された切り抜き領域の幅（ピクセル単位）。 |
| 高さ | `xsd:int` | はい | 計算された切り抜き領域の高さ（ピクセル単位）。 |

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

---
description: 画像の背景色または透明度に基づいて、画像の切り抜かれた領域を返します。
seo-description: 画像の背景色または透明度に基づいて、画像の切り抜かれた領域を返します。
seo-title: getAutoCropRect
solution: Experience Manager
title: getAutoCropRect
topic: Dynamic Media Image Production System API
uuid: bb00d89a-5fc4-476f-aa47-3cf69ef99afe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 13%

---


# getAutoCropRect{#getautocroprect}

画像の背景色または透明度に基づいて、画像の切り抜かれた領域を返します。

構文

## 認証済みユーザータイプ{#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**入力(getAutoCropRectParam)**

>[!NOTE]
>
>このメソッドを呼び出すときは、`*`autoColorCropOptions`*`または`*`autoTransparentCropOptions`*`を指定します。

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 操作するアセットを含む会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | 操作するアセットのハンドル。 |
| `*`autoColorCropOptions`*` | `types:AutoColorCropOptions` | いいえ | 色に基づいて切り抜き長方形を計算します。 [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)を参照してください。 |
| `*`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | いいえ | 透明度に基づいて切り抜き長方形を計算します。 [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)を参照してください。 |

**出力(getAutoCropRectReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`xOffset`*` | `xsd:int` | はい | 計算された切り抜き領域の左の開始ピクセル座標です。 |
| `*`yOffset`*` | `xsd:int` | はい | 計算された切り抜き領域の開始の上部ピクセル座標です。 |
| `*`width`*` | `xsd:int` | はい | 計算された切り抜き領域の幅（ピクセル単位）。 |
| `*`height`*` | `xsd:int` | はい | 計算された切り抜き領域の高さ（ピクセル単位）。 |

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


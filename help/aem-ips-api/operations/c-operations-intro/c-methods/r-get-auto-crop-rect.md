---
description: 背景色または透明度に基づいて画像の切り抜き領域を返します。
seo-description: 背景色または透明度に基づいて画像の切り抜き領域を返します。
seo-title: getAutoCropRect
solution: Experience Manager
title: getAutoCropRect
topic: Scene7 Image Production System API
uuid: bb00d89a-5fc4-476f-aa47-3cf69ef99afe
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# getAutoCropRect{#getautocroprect}

背景色または透明度に基づいて画像の切り抜き領域を返します。

構文

## 認証されたユーザータイプ {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

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
>このメソッドを呼び ` *`出すときは`*` 、 ` *`autoColorCropOptions`*` またはautoTransparentCropOptionsを指定します。

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 操作するアセットを持つ会社のハンドル。 |
| ` *`assetHandle`*` | `xsd:string` | はい | 操作するアセットのハンドル。 |
| ` *`autoColorCropOptions`*` | `types:AutoColorCropOptions` | いいえ | 色に基づいて切り抜き長方形を計算します。 AutoColorCropOptionsを参照し [てください](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)。 |
| ` *`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | いいえ | 透明度に基づいて切り抜き長方形を計算します。 AutoTransparentCropOptionsを参照し [てください](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)。 |

**出力(getAutoCropRectReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`xOffset`*` | `xsd:int` | はい | 計算された切り抜き領域の開始左ピクセル座標です。 |
| ` *`yOffset`*` | `xsd:int` | はい | 計算された切り抜き領域の開始先のピクセル座標。 |
| ` *`width`*` | `xsd:int` | はい | 計算された切り抜き領域の幅（ピクセル単位）。 |
| ` *`height`*` | `xsd:int` | はい | 計算された切り抜き領域の高さ（ピクセル単位）。 |

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


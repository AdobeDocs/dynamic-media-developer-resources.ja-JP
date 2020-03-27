---
description: 画像をシャープにします。 layer=compの場合、基本的なシャープフィルターをレイヤーまたは最終的なビュー画像に適用します。
seo-description: 画像をシャープにします。 layer=compの場合、基本的なシャープフィルターをレイヤーまたは最終的なビュー画像に適用します。
seo-title: op_sharpen
solution: Experience Manager
title: op_sharpen
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a00c60a-0d5c-4a99-a649-f29ebd710cf3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_sharpen{#op-sharpen}

画像をシャープにします。 layer=compの場合、基本的なシャープフィルターをレイヤーまたは最終的なビュー画像に適用します。

`op_sharpen=0|1`

レイヤーマスクや合成マスクにもシャープが適用されます。

## プロパティ {#section-b27f3f6a27c34233b3f76805e18b2aa7}

レイヤー属性またはビュー属性。 現在のレイヤーまたは最終ビュー画像（の場合）に適用されま `layer=comp`す。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`に設定します。

## 例 {#section-3202122df5db4e14b358ecabfb6d8b85}

画像の再サンプリングによるかすかなぼかしを補正します。 また、シャープの適用されたエッジに沿ってJPEGのアーチファクトが増えないように、JPEGの画質を高めます。

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 関連項目 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)

---
description: 画像をシャープにします。 layer=compの場合に、基本的なシャープフィルターをレイヤーまたは最終的なビュー画像に適用します。
solution: Experience Manager
title: op_sharpen
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# op_sharpen{#op-sharpen}

画像をシャープにします。 layer=compの場合に、基本的なシャープフィルターをレイヤーまたは最終的なビュー画像に適用します。

`op_sharpen=0|1`

レイヤーマスクやコンポジットマスクもシャープにされます。

## プロパティ {#section-b27f3f6a27c34233b3f76805e18b2aa7}

画層属性またはビュー属性。 `layer=comp`の場合は、現在の画層または最終ビュー画像に適用されます。 エフェクトレイヤでは無視されます。

## 初期設定 {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`（シャープ効果なし）

## 例 {#section-3202122df5db4e14b358ecabfb6d8b85}

画像の再サンプリングによって生じるわずかなぼかしを補正します。 また、シャープにされるエッジに沿ったJPEGアーティファクトが追加されないように、JPEGの画質も向上します。

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 関連項目 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)

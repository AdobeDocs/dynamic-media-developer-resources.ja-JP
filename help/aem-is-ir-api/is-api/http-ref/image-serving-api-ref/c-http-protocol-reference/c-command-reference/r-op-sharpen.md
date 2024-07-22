---
title: op_sharpen
description: 画像をシャープにする。 layer=comp の場合は、すべての拡大縮小の後、レイヤーまたは最終ビューイメージに基本的なシャープフィルターを適用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---

# op_sharpen{#op-sharpen}

画像をシャープにする。 layer=comp の場合は、すべての拡大縮小の後、レイヤーまたは最終ビューイメージに基本的なシャープフィルターを適用します。

`op_sharpen=0|1`

レイヤーマスクまたはコンポジットマスクもシャープになります。

## プロパティ {#section-b27f3f6a27c34233b3f76805e18b2aa7}

レイヤ アトリビュートまたはビューアトリビュート。 現在の画層、または `layer=comp` の場合は最終表示イメージに適用されます。 エフェクトレイヤーで無視されます。

## 初期設定 {#section-665709700fff458e9dbbf8a78e8ecf71}

シャープニング効果がない場合は `op_sharpen=0` を使用します。

## 例 {#section-3202122df5db4e14b358ecabfb6d8b85}

画像の再サンプリングによって発生するわずかなブラーを補正します。 また、JPEGの質を高めて、鋭利なエッジに沿ってJPEGのアーチファクトが発生しないようにします。

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## 関連項目 {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)

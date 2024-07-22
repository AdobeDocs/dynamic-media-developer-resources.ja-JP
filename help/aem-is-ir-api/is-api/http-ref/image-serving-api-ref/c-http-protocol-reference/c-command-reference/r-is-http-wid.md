---
title: wid
description: ビューの幅 リクエストに fit=がない場合の応答画像（ビュー画像）の幅を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---

# wid{#wid}

ビューの幅 リクエストに fit=がない場合の応答画像（ビュー画像）の幅を指定します。

`wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位）（0 より大きい整数）。 </p> </td> 
 </tr> 
</table>

`hei=` と `scl=` の両方を指定した場合、`align=` 属性に従って合成画像が切り抜かれる可能性があります。 `fit=` が存在する場合、`wid=` は、応答イメージの正確な幅、最小の幅、最大の幅を指定します。詳細については、`fit=` の説明を参照してください。

`scl=` が指定されていない場合、合成画像はサイズに合わせて調整されます。 `wid=` と `hei=` の両方が指定され、`scl=` が指定されていない場合、イメージは wid/hei の長方形に完全に収まるように拡大縮小され、可能な限り少ない背景領域が表示されます。 この場合、画像は `align=` 属性に従ってビューの長方形内に配置されます。

>[!NOTE]
>
>計算済みまたはデフォルトの返信画像のサイズが `attribute::MaxPix` を超える場合はエラーが返されます。

## 初期設定 {#section-976d4c8554a34c899f85d172f6ac6f58}

`wid=`、`hei=`、`scl=` のいずれも指定しない場合、返信画像は合成画像のサイズまたは `attribute::DefaultPix` のどちらか小さい方のサイズになります。

## プロパティ {#section-c93b7ce1b0d2475f80b06264b45d1285}

ビュー属性。 現在のレイヤ設定に関係なく適用されます。

## 例 {#section-82bc98b7c15a451bbe9b915d414c0470}

200 x 200 の長方形に収まるように画像をリクエストし、正方形でない場合は画像を右上に揃えます。 背景の領域は `attribute::BkgColor` で埋められます。

` http:// *` サーバー `*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

同じ画像が、200 ピクセルの固定幅で配信されます。ただし、画像の縦横比を維持するために高さは可変です。 この場合、返される画像には背景の塗りつぶし領域はありません。 この場合、`align=` れは全く効果がないだろう。

` http:// *` サーバー `*/myRootId/myImageId?wid=200`

## 関連項目 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、[fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)、[attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)、[attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)

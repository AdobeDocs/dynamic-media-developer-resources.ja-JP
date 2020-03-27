---
description: ビューの幅。 fit=が要求に存在しない場合の応答画像（ビュー画像）の幅を指定します。
seo-description: ビューの幅。 fit=が要求に存在しない場合の応答画像（ビュー画像）の幅を指定します。
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# wid{#wid}

ビューの幅。 fit=が要求に存在しない場合の応答画像（ビュー画像）の幅を指定します。

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位、整数値0より大きい）。 </p> </td> 
 </tr> 
</table>

との両方を指 `hei=` 定した `scl=` 場合、属性に従って合成画像が切り抜かれる場合があ `align=` ります。 が存在 `fit=` する場合、 `wid=` 正確な応答画像の幅、最小値または最大値を指定します。詳しくは、の説明を参照し `fit=` てください。

を指定 `scl=` しない場合、合成画像はサイズに合わせて調整されます。 との両方を指 `wid=` 定し `hei=` 、指定しな `scl=` い場合、画像は幅/平角の範囲内に完全に収まるように拡大縮小され、可能な限り広がる背景領域はほとんど残りません。 この場合、画像は属性に従ってビューの長方形内に配置され `align=` ます。

>[!NOTE]
>
>計算された返信画像またはデフォルトの返信画像のサイズが次のサイズより大きい場合は、エラーが返されま `attribute::MaxPix`す。

## 初期設定 {#section-976d4c8554a34c899f85d172f6ac6f58}

どちらも指 `wid=`定さ `hei=`れていな `scl=` い場合、またはどちらも指定されていない場合、返信画像は、合成画像のサイズか、小さい方 `attribute::DefaultPix`を持ちます。

## プロパティ {#section-c93b7ce1b0d2475f80b06264b45d1285}

属性を表示します。 現在のレイヤー設定に関係なく適用されます。

## 例 {#section-82bc98b7c15a451bbe9b915d414c0470}

200 x 200の長方形に合わせて画像を要求します。画像が正方形でない場合は、右上で画像を整列します。 背景領域は塗りつぶされま `attribute::BkgColor`す。

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

同じ画像を200ピクセルの固定幅で配信し、画像の縦横比を維持するために高さを可変にします。 この場合、返される画像には背景の塗り領域がありません。 この場合、align=はまったく影響しません。

` http:// *`server`*/myRootId/myImageId?wid=200`

## 関連項目 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)[Pix Attribute: DefaultPixAttribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)

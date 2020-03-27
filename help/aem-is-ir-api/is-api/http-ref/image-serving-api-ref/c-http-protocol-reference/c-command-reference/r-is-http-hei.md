---
description: ビューの高さ fitが要求に存在しない場合の応答画像（ビュー画像）の高さを指定します。
seo-description: ビューの高さ fitが要求に存在しない場合の応答画像（ビュー画像）の高さを指定します。
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

ビューの高さ fitが要求に存在しない場合の応答画像（ビュー画像）の高さを指定します。

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>画像の高さ（ピクセル単位、整数値0より大きい）。 </p> </td> 
 </tr> 
</table>

との両方を指 `wid=` 定した `scl=` 場合、属性に従って合成画像が切り抜かれる場合があ `align=`ります。 が存在 `fit=` する場合、 `hei=` 正確な応答画像の高さ、最小値または最大値を指定します。詳しくは、の説明を参照し ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)` てください。

を指定 `scl=` しない場合、合成画像はサイズに合わせて調整されます。 との両方を指 `wid=` 定し `hei=` 、指定しな `scl=` い場合、画像は幅と高さの長方形全体に収まるように拡大縮小され、可能な限り小さな背景領域が露出します。この場合、画像は属性に従ってビューの長方形内に配置され `align=` ます。 背景領域は、またはで指定され `bgc=`ていない場合は、で塗りつぶされま `attribute::BkgColor`す。

>[!NOTE]
>
>計算された返信画像のサイズが次よりも大きい場合は、エラーが返されま `attribute::MaxPix`す。

## プロパティ {#section-534923644a1e464496eeba83dedcbd3c}

属性を表示します。 現在のレイヤー設定に関係なく適用されます。

## 初期設定 {#section-76544d34806d4124a8b173e229cba71f}

どちらも指 `wid=`定さ `hei=`れていな `scl=` い場合、またはどちらも指定されていない場合、返信画像は合成画像のサイズか、小さい方 `attribute::DefaultPix`を持ちます。

## 例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

200 x 200の長方形に合わせて画像を要求します。画像が正方形でない場合は、左上揃えにします。 背景領域は塗りつぶされま `attribute::BkgColor`す。

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

同じ画像を、200ピクセルの固定高さで配信し、画像の縦横比に合わせて可変幅で配信します。 この場合、返される画像には背景の塗り領域がありません。 この場合、全く効 `align=` 果がありません。

`http://server/myRootId/myImageId?hei=200`

## 関連項目 {#section-796e059e42ea4e86ab90ea3d024850ec}

[id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) fit= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)scl= [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [gc](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [gc](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)gc = [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)gn gc [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)[, ng =, attribute: Pix Default, pixAttribute: pix max](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)

---
description: 表示の高さ fitがリクエストに存在しない場合に、応答画像(表示画像)の高さを指定します。
seo-description: 表示の高さ fitがリクエストに存在しない場合に、応答画像(表示画像)の高さを指定します。
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 2%

---


# hei{#hei}

表示の高さ fitがリクエストに存在しない場合に、応答画像(表示画像)の高さを指定します。

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>画像の高さ（ピクセル単位、0より大きい整数） </p> </td> 
 </tr> 
</table>

`wid=`と`scl=`の両方を指定した場合、`align=`属性に従って合成画像が切り抜かれる場合があります。 `fit=`が存在する場合、`hei=`は、完全一致、最小値、または最大応答画像の高さを指定します。詳しくは、` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)`の説明を参照してください。

`scl=`を指定しない場合、合成画像はサイズに合わせて調整されます。 `wid=`と`hei=`の両方を指定し、`scl=`を指定しない場合、画像はwid/heiの長方形内に完全に収まるように拡大縮小され、できるだけ小さな背景領域が露出します。この場合、画像は`align=`属性に従って表示の長方形内に配置されます。 背景領域は`bgc=`で塗りつぶされます。指定しない場合は`attribute::BkgColor`で塗りつぶされます。

>[!NOTE]
>
>計算された返信画像のサイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## プロパティ {#section-534923644a1e464496eeba83dedcbd3c}

表示属性。 現在のレイヤー設定に関係なく適用されます。

## 初期設定 {#section-76544d34806d4124a8b173e229cba71f}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、返信画像は合成画像のサイズか`attribute::DefaultPix`のいずれか小さい方のサイズを持ちます。

## 例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

200 x 200の長方形に合わせるように画像を要求します。画像が正方形でない場合は、左上揃えにします。 背景領域はすべて`attribute::BkgColor`で塗りつぶされます。

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

同じ画像が、200ピクセルの固定高さで配信されますが、画像の縦横比に合わせて可変幅で配信されます。 この場合、返される画像には背景の塗り領域がありません。 この場合`align=`は全く効果がないことに注意してください。

`http://server/myRootId/myImageId?hei=200`

## 関連項目 {#section-796e059e42ea4e86ab90ea3d024850ec}

[id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , fit= [, scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)align= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)lign=align= [, bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), ngc ngc=ngn  [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1) [ng=natribute: Pix Pix Default, pix max, pix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)

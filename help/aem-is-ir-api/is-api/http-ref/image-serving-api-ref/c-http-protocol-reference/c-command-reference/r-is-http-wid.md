---
description: 表示の幅。 fit=がリクエストに存在しない場合の応答画像(表示画像)の幅を指定します。
seo-description: 表示の幅。 fit=がリクエストに存在しない場合の応答画像(表示画像)の幅を指定します。
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 3%

---


# wid{#wid}

表示の幅。 fit=がリクエストに存在しない場合の応答画像(表示画像)の幅を指定します。

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位、0より大きい整数） </p> </td> 
 </tr> 
</table>

`hei=`と`scl=`の両方を指定した場合、`align=`属性に従って合成画像が切り抜かれる場合があります。 `fit=`が存在する場合、`wid=`は、完全一致、最小値、または最大応答画像の幅を指定します。詳しくは、`fit=`の説明を参照してください。

`scl=`を指定しない場合、合成画像はサイズに合わせて調整されます。 `wid=`と`hei=`の両方を指定し、`scl=`を指定しない場合、画像はwid/heiの長方形内に完全に収まるように拡大縮小され、できるだけ小さな背景領域が露出します。 この場合、画像は`align=`属性に従って表示の長方形内に配置されます。

>[!NOTE]
>
>計算済みまたはデフォルトの返信画像のサイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## 初期設定 {#section-976d4c8554a34c899f85d172f6ac6f58}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、返信画像は合成画像のサイズか`attribute::DefaultPix`のいずれか小さい方のサイズになります。

## プロパティ {#section-c93b7ce1b0d2475f80b06264b45d1285}

表示属性。 現在のレイヤー設定に関係なく適用されます。

## 例 {#section-82bc98b7c15a451bbe9b915d414c0470}

200 x 200の長方形に合わせるように画像を要求します。画像が正方形でない場合は、右上揃えにします。 背景領域はすべて`attribute::BkgColor`で塗りつぶされます。

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

同じ画像を200ピクセルの固定幅で配信し、高さは可変で画像の縦横比を維持します。 この場合、返される画像には背景の塗り領域がありません。 この場合、align=はまったく影響しません。

` http:// *`server`*/myRootId/myImageId?wid=200`

## 関連項目 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) ,  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), align= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)align= [, ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1) [attribute: Default PixFit, attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)

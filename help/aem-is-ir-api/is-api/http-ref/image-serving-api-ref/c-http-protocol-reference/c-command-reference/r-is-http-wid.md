---
description: ビューの幅。 fit=がリクエストに存在しない場合の応答画像（ビュー画像）の幅を指定します。
solution: Experience Manager
title: wid
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 3%

---

# wid{#wid}

ビューの幅。 fit=がリクエストに存在しない場合の応答画像（ビュー画像）の幅を指定します。

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位、0より大きい整数） </p> </td> 
 </tr> 
</table>

`hei=`と`scl=`の両方を指定した場合、 `align=`属性に従って合成画像を切り抜くことができます。 `fit=`が存在する場合、`wid=`は応答画像の幅（最小値または最大値）を指定します。詳しくは、 `fit=`の説明を参照してください。

`scl=`を指定しない場合、合成画像は合わせて拡大縮小されます。 `wid=`と`hei=`の両方を指定し、`scl=`を指定しない場合、画像はwid/heiの長方形内に収まるように拡大/縮小され、可能な限り背景領域が露出しないようになります。 この場合、画像は`align=`属性に従ってビューの長方形内に配置されます。

>[!NOTE]
>
>計算された返信画像サイズまたはデフォルトの返信画像サイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## 初期設定 {#section-976d4c8554a34c899f85d172f6ac6f58}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、返信画像は合成画像のサイズか`attribute::DefaultPix`のどちらか小さい方になります。

## プロパティ {#section-c93b7ce1b0d2475f80b06264b45d1285}

属性を表示します。 現在の画層設定に関係なく適用されます。

## 例 {#section-82bc98b7c15a451bbe9b915d414c0470}

200 x 200の長方形に収まるように画像を要求します。画像が正方形でない場合は、右上揃えにします。 背景領域は`attribute::BkgColor`で塗りつぶされます。

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

同じ画像が、200ピクセルの固定幅で配信されますが、高さが可変で、画像の縦横比を維持します。 この場合、返される画像には背景の塗り領域はありません。 この場合、 align=はまったく効果を持ちません。

` http:// *`server`*/myRootId/myImageId?wid=200`

## 関連項目 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) 、 [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)、 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、 [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)、 [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)、 [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)

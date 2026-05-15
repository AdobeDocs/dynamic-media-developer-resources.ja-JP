---
title: wid
description: ビューの幅： fit=がリクエストに存在しない場合の応答イメージ（ビュー画像）の幅を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
TQID: 'https://experienceleague.adobe.com/n6U4pPJuxOo3rX2nU7EYsnevrCPBzoYq5SiQvrr5t20'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 274
ht-degree: 1%

---

# wid{#wid}

ビューの幅： fit=がリクエストに存在しない場合の応答イメージ（ビュー画像）の幅を指定します。

`wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>画像の幅（0より大きい整数）。 </p> </td> 
 </tr> 
</table>

`hei=`と`scl=`の両方が指定されている場合、`align=`属性に従って合成画像が切り抜かれる可能性があります。 `fit=`が存在する場合、`wid=`は正確、最小、または最大応答画像幅を指定します。詳しくは、`fit=`の説明を参照してください。

`scl=`が指定されていない場合、合成イメージはフィットするように拡大・縮小されます。 `wid=`と`hei=`の両方が指定されていて、`scl=`が指定されていない場合、画像は幅/高さの長方形の中に完全に収まるように拡大/縮小され、背景の露出をできる限り少なくします。 この場合、画像は`align=`属性に従ってビュー長方形の中に配置されます。

>[!NOTE]
>
>計算された返信画像サイズまたはデフォルトの返信画像サイズが`attribute::MaxPix`を超える場合は、エラーが返されます。

## 初期設定 {#section-976d4c8554a34c899f85d172f6ac6f58}

`wid=`、`hei=`および`scl=`のいずれも指定されていない場合、返信画像は、合成画像のサイズまたは`attribute::DefaultPix`のいずれか小さいサイズになります。

## プロパティ {#section-c93b7ce1b0d2475f80b06264b45d1285}

ビュー属性。 現在のレイヤー設定に関係なく適用されます。

## 例 {#section-82bc98b7c15a451bbe9b915d414c0470}

200 x 200の長方形に収まるように画像を要求します。画像が正方形でない場合は、右上に配置します。 背景の領域は`attribute::BkgColor`で塗りつぶされています。

` http:// *` サーバー`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

同じ画像が200 ピクセルの固定幅で配信されますが、画像の縦横比を維持するために高さが可変です。 この場合、返される画像には背景塗りつぶし領域がありません。 この場合、`align=`はまったく効果がありません。

` http:// *` サーバー`*/myRootId/myImageId?wid=200`

## 関連項目 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、[fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)、[属性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)、[属性：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)

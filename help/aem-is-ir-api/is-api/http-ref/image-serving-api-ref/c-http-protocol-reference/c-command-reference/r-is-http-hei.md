---
title: へい
description: 高さを表示します。 要求に適合しない場合の応答画像（ビュー画像）の高さを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
TQID: 'https://experienceleague.adobe.com/KzBsUuPz9BcMOMuNqPx-kNaoAKuKDlCy1qL4hkPCv-A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 1%

---

# へい{#hei}

高さを表示します。 要求に適合しない場合の応答画像（ビュー画像）の高さを指定します。

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>画像の高さ（0 （0）より大きい値）。 </p> </td> 
 </tr> 
</table>

`wid=`と`scl=`の両方が指定されている場合、合成画像は`align=`属性に従って切り抜かれる可能性があります。 `fit=`が存在する場合、`hei=`は正確、最小、または最大応答画像の高さを指定します。詳細については、[fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md)の説明を参照してください。

`scl=`が指定されていない場合、合成イメージはフィットするように拡大・縮小されます。 `wid=`と`hei=`の両方が指定されていて、`scl=`が指定されていない場合、画像は幅/高さの長方形の中に完全に収まるように拡大/縮小され、背景の露出をできる限り少なくします。 この場合、画像は`align=`属性に従ってビュー長方形の中に配置されます。 背景の領域が`bgc=`で塗りつぶされています。または、`attribute::BkgColor`で指定されていない場合は、塗りつぶされます。

>[!NOTE]
>
>計算された返信画像のサイズが`attribute::MaxPix`より大きい場合、エラーが返されます。

## プロパティ {#section-534923644a1e464496eeba83dedcbd3c}

ビュー属性。 現在のレイヤー設定に関係なく適用されます。

## 初期設定 {#section-76544d34806d4124a8b173e229cba71f}

`wid=`、`hei=`および`scl=`のいずれも指定されていない場合、返信画像は、合成画像のサイズまたは`attribute::DefaultPix`のいずれか小さいサイズになります。

## 例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

200 x 200の長方形に収まるように画像を要求します。画像が正方形でない場合は、左上に配置します。 背景の領域は`attribute::BkgColor`で塗りつぶされています。

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

同じ画像が、200 ピクセルの固定された高さで配信されますが、画像の縦横比に合わせて幅が可変です。 この場合、返される画像には背景塗りつぶし領域がありません。 この場合、`align=`はまったく効果がありません。

`http://server/myRootId/myImageId?hei=200`

## 関連項目 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)、[bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)、[rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)、[属性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)、[属性：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)

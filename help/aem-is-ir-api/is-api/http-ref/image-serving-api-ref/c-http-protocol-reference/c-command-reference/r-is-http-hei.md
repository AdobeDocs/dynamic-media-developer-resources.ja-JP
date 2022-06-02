---
description: ビューの高さ リクエストに fit が存在しない場合の応答画像（画像の表示）の高さを指定します。
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 2%

---

# hei{#hei}

ビューの高さ リクエストに fit が存在しない場合の応答画像（画像の表示）の高さを指定します。

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>画像の高さ（ピクセル単位、整数値 0 以上）。 </p> </td> 
 </tr> 
</table>

両方の `wid=` および `scl=` を指定した場合、 `align=`属性。 条件 `fit=` が存在する場合 `hei=` 応答画像の高さ（最小値）を正確に指定します。説明を参照する [fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) 」を参照してください。

If `scl=` を指定しない場合、合成画像はサイズに合わせて拡大縮小されます。 両方の `wid=` および `hei=` が指定され、 `scl=` が指定されていない場合、画像は幅/平の長方形内に完全に収まるように拡大縮小され、可能な限り背景領域が露出しなくなります。この場合、画像は、 `align=` 属性。 背景領域は `bgc=`、またはで指定されていない場合は `attribute::BkgColor`.

>[!NOTE]
>
>計算された返信画像のサイズが次のサイズを超える場合は、エラーが返されます `attribute::MaxPix`.

## プロパティ {#section-534923644a1e464496eeba83dedcbd3c}

属性を表示します。 現在の画層設定に関係なく適用されます。

## 初期設定 {#section-76544d34806d4124a8b173e229cba71f}

どちらも `wid=`, `hei=`または `scl=` を指定した場合、返信画像は合成画像のサイズか `attribute::DefaultPix`（どちらか小さい方）

## 例 {#section-eb10df7cd67e4733984810aaffd0b9e2}

200 x 200 の長方形に収まるように画像を要求します。画像が正方形でない場合は、左上揃えになります。 背景領域は `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

同じ画像が、200 ピクセルの固定された高さで配信されますが、画像の縦横比に合わせて可変幅になります。 この場合、返される画像に背景の塗り領域は含まれません。 この場合、 `align=` 全く効果がなかっただろう

`http://server/myRootId/myImageId?hei=200`

## 関連項目 {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)

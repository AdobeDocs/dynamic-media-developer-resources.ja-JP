---
description: 拡大・縮小表示 invFactorの逆数で合成画像を拡大・縮小します。
seo-description: 拡大・縮小表示 invFactorの逆数で合成画像を拡大・縮小します。
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

拡大・縮小表示 invFactorの逆数で合成画像を拡大・縮小します。

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>逆スケール係数（0.0より大きい実数） </p></td> 
 </tr> 
</table>

No scaling is applied when `scl=1`. *`invFactor`* 1.0より大きく、1.0より小さい場合は、合成画像が拡大されます。

を指定 `scl=` した場合、および `wid=` /またはが `hei=` 同じように存在する場合、画像は縮小後に切り抜か `wid=` れたり切り `hei=` 抜かれたりします。

>[!NOTE]
>
>計算された返信画像またはデフォルトの返信画像のサイズが次のサイズより大きい場合は、エラーが返されま `attribute::MaxPix`す。

## プロパティ {#section-60af012719db477db4a4703e9a6da5f5}

属性の表示 現在のレイヤー設定に関係なく適用されます。

## 初期設定 {#section-32502fa218a24e1f9c65f41c0260b56a}

どちらも指 `wid=`定さ `hei=`れていな `scl=` い場合、またはどちらも指定されていない場合、返信画像は、合成画像のサイズか、小さい方 `attribute::DefaultPix`を持ちます。

## 例 {#section-a33f6239476a4b438d939656ad99aa76}

の一般的な用途につ [いては、](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) rotate=の例を参照してくださ `scl=`い。

## 関連項目 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

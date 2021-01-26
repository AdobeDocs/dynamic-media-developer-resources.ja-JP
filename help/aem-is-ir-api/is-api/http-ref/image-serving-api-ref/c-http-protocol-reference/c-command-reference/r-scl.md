---
description: スケール表示 invFactorの逆数で合成画像を拡大・縮小します。
seo-description: スケール表示 invFactorの逆数で合成画像を拡大・縮小します。
seo-title: scl
solution: Experience Manager
title: scl
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 5%

---


# scl{#scl}

スケール表示 invFactorの逆数で合成画像を拡大・縮小します。

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>逆スケール係数（0.0より大きい実数） </p></td> 
 </tr> 
</table>

`scl=1`の場合、拡大/縮小は適用されません。 *`invFactor`* 1.0より大きい場合は縮小表示され、1.0より小さい場合は合成画像が拡大されます。

`scl=`を指定し、`wid=`や`hei=`も存在する場合、画像は縮小後に`wid=`や`hei=`に切り抜かれます。

>[!NOTE]
>
>計算済みまたはデフォルトの返信画像のサイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## プロパティ {#section-60af012719db477db4a4703e9a6da5f5}

表示属性。 現在のレイヤー設定に関係なく適用されます。

## 初期設定 {#section-32502fa218a24e1f9c65f41c0260b56a}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、返信画像は合成画像のサイズか`attribute::DefaultPix`のいずれか小さい方のサイズになります。

## 例 {#section-a33f6239476a4b438d939656ad99aa76}

`scl=`の一般的な用途については、[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)の例を参照してください。

## 関連項目 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

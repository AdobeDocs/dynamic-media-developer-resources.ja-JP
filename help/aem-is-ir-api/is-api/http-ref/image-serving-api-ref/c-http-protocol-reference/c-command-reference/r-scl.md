---
title: scl
description: ビューを拡大/縮小します。 invFactor の逆の値で合成画像を拡大/縮小します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# scl{#scl}

ビューを拡大/縮小します。 invFactor の逆の値で合成画像を拡大/縮小します。

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>逆尺度係数（0.0 より大きい実数） </p></td> 
 </tr> 
</table>

`scl=1` の場合、拡大縮小は適用されません。 1.0 より大きいダウンスケールと 1.0 より小さい *`invFactor`* 値は、合成画像を拡大します。

`scl=` が指定され、`wid=` や `hei=` も存在する場合、拡大縮小の後に画像が `wid=` や `hei=` に切り抜かれます。

>[!NOTE]
>
>計算済みまたはデフォルトの返信画像のサイズが `attribute::MaxPix` を超える場合はエラーが返されます。

## プロパティ {#section-60af012719db477db4a4703e9a6da5f5}

ビュー属性。 現在のレイヤ設定に関係なく適用されます。

## 初期設定 {#section-32502fa218a24e1f9c65f41c0260b56a}

`wid=`、`hei=`、`scl=` のいずれも指定しない場合、返信画像は合成画像のサイズまたは `attribute::DefaultPix` のどちらか小さい方のサイズになります。

## 例 {#section-a33f6239476a4b438d939656ad99aa76}

[ の一般的な用途については、](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)rotate=`scl=` の例を参照してください。

## 関連項目 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

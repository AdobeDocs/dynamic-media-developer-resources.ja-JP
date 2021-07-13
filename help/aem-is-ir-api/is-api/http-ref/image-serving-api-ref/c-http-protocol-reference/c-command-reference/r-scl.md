---
description: 拡大・縮小ビュー invFactorの逆数で合成イメージを拡大/縮小します。
solution: Experience Manager
title: scl
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---

# scl{#scl}

拡大・縮小ビュー invFactorの逆数で合成イメージを拡大/縮小します。

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>逆スケール係数（0.0より大きい実数） </p></td> 
 </tr> 
</table>

`scl=1`の場合、スケーリングは適用されません。 *`invFactor`* 1.0より大きく、1.0より小さい場合は、合成画像が拡大されます。

`scl=`を指定し、`wid=`や`hei=`も指定した場合、画像は拡大縮小後に`wid=`や`hei=`に切り抜かれます。

>[!NOTE]
>
>計算された返信画像サイズまたはデフォルトの返信画像サイズが`attribute::MaxPix`より大きい場合は、エラーが返されます。

## プロパティ {#section-60af012719db477db4a4703e9a6da5f5}

属性を表示 現在の画層設定に関係なく適用されます。

## 初期設定 {#section-32502fa218a24e1f9c65f41c0260b56a}

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合、返信画像は合成画像のサイズか`attribute::DefaultPix`のどちらか小さい方になります。

## 例 {#section-a33f6239476a4b438d939656ad99aa76}

`scl=`の一般的な適用については、[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)の例を参照してください。

## 関連項目 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

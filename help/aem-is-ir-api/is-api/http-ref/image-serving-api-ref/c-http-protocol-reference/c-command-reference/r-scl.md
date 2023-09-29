---
title: scl
description: 拡大・縮小表示。 invFactor の逆数で合成イメージの尺度を変更します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 4%

---

# scl{#scl}

拡大・縮小表示。 invFactor の逆数で合成イメージの尺度を変更します。

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>逆スケール係数（0.0 より大きい実数） </p></td> 
 </tr> 
</table>

スケーリングは適用されません。 `scl=1`. An *`invFactor`* 1.0 より大きく、1.0 より小さい値を指定すると、合成イメージが拡大されます。

次の場合 `scl=` が指定され、 `wid=` および/または `hei=` が存在する場合は、画像は次の場所に切り抜かれます。 `wid=` および/または `hei=` 拡大・縮小後

>[!NOTE]
>
>返信画像のサイズが計算済みまたはデフォルトより大きい場合は、エラーが返されます。 `attribute::MaxPix`.

## プロパティ {#section-60af012719db477db4a4703e9a6da5f5}

属性を表示します。 現在の画層設定に関係なく適用されます。

## 初期設定 {#section-32502fa218a24e1f9c65f41c0260b56a}

どちらでもない場合 `wid=`, `hei=`または `scl=` を指定した場合、返信画像は合成画像のサイズか、 `attribute::DefaultPix`（どちらか小さい方）

## 例 {#section-a33f6239476a4b438d939656ad99aa76}

詳しくは、 [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ～の共通の用途のために `scl=`.

## 関連項目 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

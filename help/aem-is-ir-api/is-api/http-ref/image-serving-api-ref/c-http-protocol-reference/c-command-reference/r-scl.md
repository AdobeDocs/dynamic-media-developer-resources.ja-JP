---
title: scl
description: 拡大・縮小ビュー。 合成画像をinvFactorの逆に拡大・縮小します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
TQID: 'https://experienceleague.adobe.com/Evu9NXhBJE-Z4inLuaWJkiJikd2yslhec5q7C2azxKw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 2%

---

# scl{#scl}

拡大・縮小ビュー。 合成画像をinvFactorの逆に拡大・縮小します。

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>スケール因子の反転（0.0より大きい値） </p></td> 
 </tr> 
</table>

`scl=1`の場合、拡大・縮小は適用されません。 ダウンスケールが1.0より大きく1.0より小さい&#x200B;*`invFactor`*&#x200B;値は、合成画像を拡大します。

`scl=`が指定されており、`wid=`および/または`hei=`も存在する場合、画像は拡大縮小後に`wid=`または`hei=`に切り抜かれます。

>[!NOTE]
>
>計算された返信画像サイズまたはデフォルトの返信画像サイズが`attribute::MaxPix`を超える場合は、エラーが返されます。

## プロパティ {#section-60af012719db477db4a4703e9a6da5f5}

属性を表示します。 現在のレイヤー設定に関係なく適用されます。

## 初期設定 {#section-32502fa218a24e1f9c65f41c0260b56a}

`wid=`、`hei=`および`scl=`のいずれも指定されていない場合、返信画像は、合成画像のサイズまたは`attribute::DefaultPix`のいずれか小さいサイズになります。

## 例 {#section-a33f6239476a4b438d939656ad99aa76}

`scl=`の一般的なアプリケーションについては、[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)の例を参照してください。

## 関連項目 {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、[属性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

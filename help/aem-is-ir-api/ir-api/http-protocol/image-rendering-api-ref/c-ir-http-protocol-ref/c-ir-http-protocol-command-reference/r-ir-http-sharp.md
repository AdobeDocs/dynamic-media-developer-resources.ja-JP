---
description: テクスチャをシャープにします。 このマテリアルをレンダリングする際に適用するシャープを指定します。
solution: Experience Manager
title: 鋭い
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 6%

---

# 鋭い{#sharp}

テクスチャをシャープにします。 このマテリアルをレンダリングする際に適用するシャープを指定します。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>シャープは適用されません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>通常のシャープニング（遅く）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0個の代替シャープニング（初期）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>よりシャープにする（早期と後期）。 </p> </td> 
 </tr> 
</table>

`sharp=1` マテリアルのレンダリング後にシャープが適用されます。 `sharp=2` テクスチャを最初にスケーリングした後、シーンに変換する前に、シャープを適用します。 `sharp=3` 変換の前と後の両方にシャープを適用します。

シャープのアルゴリズムとシャープの量、およびその他のUSM（アンシャープマスク）パラメータは、ビネットが提供するデフォルトの材料テンプレートまたは`rs=`を使用して制御されます。

## プロパティ {#section-498ec9fcb8eb415fb99532d36c11d4c7}

マテリアル属性。 べた塗りマテリアルでは無視されます。

## 初期設定 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`（マテリアルがカタログエントリに基づく場合）、それ以外の場合 `attribute::Sharp`。

## 関連項目 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e),  [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)

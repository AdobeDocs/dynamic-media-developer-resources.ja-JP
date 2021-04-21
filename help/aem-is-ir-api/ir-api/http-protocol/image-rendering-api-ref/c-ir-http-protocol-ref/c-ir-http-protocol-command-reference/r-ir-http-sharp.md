---
description: テクスチャをシャープにします。 このマテリアルをレンダリングするときに適用するシャープを指定します。
solution: Experience Manager
title: 鋭い
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 6%

---


# シャープ{#sharp}

テクスチャをシャープにします。 このマテリアルをレンダリングするときに適用するシャープを指定します。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>シャープなし </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>通常のシャープの適用（遅くなりました） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0代替シャープ（初期） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>シャープの適用が増えました（早い方と遅い方）。 </p> </td> 
 </tr> 
</table>

`sharp=1` マテリアルをレンダリングした後にシャープを適用します。 `sharp=2` テクスチャを最初にスケールした後、シーンに変換する前に、シャープを適用します。 `sharp=3` 変換の前後にシャープを適用します。

シャープの適用アルゴリズムとシャープの適用量、および他のUSM（アンシャープマスク）パラメータは、ビネットが提供する初期設定のマテリアルテンプレートまたは`rs=`を使用して制御されます。

## プロパティ {#section-498ec9fcb8eb415fb99532d36c11d4c7}

マテリアル属性 べた塗りのマテリアルでは無視されます。

## 初期設定 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`材料がカタログエントリに基づいている場合は、それ以外の場合は、 `attribute::Sharp`。

## 関連項目 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e),  [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)

---
title: 鋭い
description: テクスチャをシャープにします。 このマテリアルのレンダリング時に適用するシャープを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 6%

---

# 鋭い{#sharp}

テクスチャをシャープにします。 このマテリアルのレンダリング時に適用するシャープを指定します。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>シャープは適用されません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>通常のシャープ（遅く） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 個の代替シャープニング（早期）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>シャープ（早い方と遅い方）が多い。 </p> </td> 
 </tr> 
</table>

`sharp=1` マテリアルがレンダリングされた後にシャープを適用します。 `sharp=2` テクスチャを初めてスケーリングした後、ただしシーンに変換する前にシャープを適用します。 `sharp=3` 変換前と変換後の両方にシャープを適用します。

シャープアルゴリズムとシャープの量、およびその他の USM（アンシャープマスク）のパラメータは、ビネットが提供するデフォルトのマテリアルテンプレートで制御するか、 `rs=`.

## プロパティ {#section-498ec9fcb8eb415fb99532d36c11d4c7}

材料属性。 べた塗りのマテリアルでは無視されます。

## 初期設定 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`マテリアルがカタログエントリに基づく場合は、それ以外の場合は `attribute::Sharp`.

## 関連項目 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)

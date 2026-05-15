---
title: シャープ
description: シャープテクスチャ： このマテリアルをレンダリングするときに適用するシャープを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
TQID: 'https://experienceleague.adobe.com/AWUw6E0xSWAsMfijewBvnSC8JdM5l9-qtFNLZsweFRY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 5%

---

# シャープ{#sharp}

シャープテクスチャ： このマテリアルをレンダリングするときに適用するシャープを指定します。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>シャープなし。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>通常のシャープ補正（遅い）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0の代替シャープ（早期）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>よりシャープにする（早い場合と遅い場合） </p> </td> 
 </tr> 
</table>

`sharp=1` マテリアルをレンダリングした後にシャープを適用します。`sharp=2`はテクスチャの初期スケーリング後にシャープを適用しますが、シーンに変換する前にシャープを適用します。`sharp=3`はトランスフォームの前と後の両方にシャープを適用します。

シャープニングアルゴリズムとシャープの量およびその他のUSM （アンシャープマスク）パラメーターは、ビネットまたは`rs=`を使用して提供されるデフォルトのマテリアルテンプレートによって制御されます。

## プロパティ {#section-498ec9fcb8eb415fb99532d36c11d4c7}

マテリアル属性： 単色のマテリアルでは無視されます。

## 初期設定 {#section-febfa16e65864987b4d328e2ff1df64d}

資料がカタログ エントリに基づいている場合は`catalog::Sharp`、そうでない場合は`attribute::Sharp`。

## 関連項目 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[ カタログ：：シャープ ](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0)、[ シャープ=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e)、[rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)

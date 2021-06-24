---
description: アンシャープマスク レイヤー=コンポジトの場合、すべての拡大縮小の後に、レイヤーまたは最終的なビュー画像をアンシャープマスクします。
solution: Experience Manager
title: op_usmR
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

---

# op_usmR{#op-usmr}

アンシャープマスク レイヤー=コンポジトの場合、すべての拡大縮小の後に、レイヤーまたは最終的なビュー画像をアンシャープマスクします。

ダウンサンプリングが発生したかどうかに関係なく、パラメーターはそのまま適用されます。

`op_usmR= *``*[, *``*[, *``*[, *`amountradiusRthresholdmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 値</span></span> </p></td> 
  <td class="stentry"> <p>フィルターの強さ係数（実数0 ～ 5） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>カーネル半径をピクセル単位（実数0 ～ 250）で表します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> しきい値</span></span> </p></td> 
  <td class="stentry"> <p>フィルターしきい値レベル（整数0 ～ 255）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> モノクロ</span></span> </p></td> 
  <td class="stentry"> <p>各カラーコンポーネントに個別に適用する場合は0に、画像の明るさ（強さ）にのみ適用する場合は1に設定します。 </p> <p><span class="codeph"> <span class="varname"> グレースケール画像ではmonochromeisは無視されます。</span></span>  </p> </td> 
 </tr> 
</table>

レイヤーマスクやコンポジットマスクもシャープにされます。

## プロパティ {#section-fb5311b34d164946b74dadb32359518a}

画層属性またはビュー属性。 `layer=comp`の場合は、現在の画層または最終ビュー画像に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` アンシャープマスク効果がない。

## 関連項目 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)

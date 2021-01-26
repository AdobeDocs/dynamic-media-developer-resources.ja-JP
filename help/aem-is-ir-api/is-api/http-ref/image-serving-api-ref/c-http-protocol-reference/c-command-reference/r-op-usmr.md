---
description: アンシャープマスク layer=compの場合、すべての拡大・縮小の後、レイヤーまたは最終的な表示の画像をアンシャープマスクします。
seo-description: アンシャープマスク layer=compの場合、すべての拡大・縮小の後、レイヤーまたは最終的な表示の画像をアンシャープマスクします。
seo-title: op_usmR
solution: Experience Manager
title: op_usmR
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 98afd83c-097e-40b4-b0a6-647f70b95fae
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---


# op_usmR{#op-usmr}

アンシャープマスク layer=compの場合、すべての拡大・縮小の後、レイヤーまたは最終的な表示の画像をアンシャープマスクします。

ダウンサンプリングが発生したかどうかに関係なく、パラメータはそのまま適用されます。

`op_usmR= *``*[, *``*[, *``*[, *`amountradiusRthresholdmonochromo`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 値</span></span> </p></td> 
  <td class="stentry"> <p>フィルタ強度係数（実数0 ～ 5） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p></td> 
  <td class="stentry"> <p>フィルタカーネルの半径（ピクセル単位、実数0 ～ 250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> しきい値</span></span> </p></td> 
  <td class="stentry"> <p>フィルターしきい値（整数0 ～ 255）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monichrome</span></span> </p></td> 
  <td class="stentry"> <p>各カラーコンポーネントに個別に適用する場合は0に、画像の明るさ（適用度）にのみ適用する場合は1に設定します。 </p> <p><span class="codeph"> <span class="varname"> グレースケール画像では</span></span> monochromeisは無視されます。 </p> </td> 
 </tr> 
</table>

レイヤーマスクまたはコンポジットマスクにもシャープが適用されます。

## プロパティ {#section-fb5311b34d164946b74dadb32359518a}

レイヤー属性または表示属性。 `layer=comp`の場合は、現在のレイヤーまたは最終表示の画像に適用されます。 効果レイヤーでは無視されます。

## 初期設定 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` アンシャープマスク効果がない

## 関連項目 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)

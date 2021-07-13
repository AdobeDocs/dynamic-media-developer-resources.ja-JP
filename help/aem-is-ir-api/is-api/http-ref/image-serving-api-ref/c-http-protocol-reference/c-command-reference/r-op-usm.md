---
description: アンシャープマスク レイヤー=コンポジトの場合、すべての拡大縮小の後に、レイヤーまたは最終的なビュー画像をアンシャープマスクします。
solution: Experience Manager
title: op_usm
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 6%

---

# op_usm{#op-usm}

アンシャープマスク レイヤー=コンポジトの場合、すべての拡大縮小の後に、レイヤーまたは最終的なビュー画像をアンシャープマスクします。

パラメーターは、最大解像度の画像に適用されると想定され、ダウンサンプリングされた画像を処理する際に縮小されます。

`op_usm= *``*[, *``*[, *``*[, *`amountradiusthresholdmonochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 値</span></span> </p></td> 
  <td class="stentry"> <p>フィルターの強さ係数（実数0 ～ 5） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p></td> 
  <td class="stentry"> <p>カーネル半径をピクセル単位（実数0 ～ 250）で表します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> しきい値</span></span> </p></td> 
  <td class="stentry"> <p>フィルターしきい値レベル（整数0 ～ 255）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> モノクロ</span></span> </p></td> 
  <td class="stentry"> <p>各カラーコンポーネントに個別に適用する場合は0に、画像の明るさ（強さ）にのみ適用する場合は1に設定します。 </p> <p> <span class="codeph"><span class="varname"> グレースケール画像ではmonochromeisは無視されます。</span></span>  </p></td> 
 </tr> 
</table>

レイヤーマスクやコンポジットマスクもシャープにされます。

## プロパティ {#section-fb5311b34d164946b74dadb32359518a}

画層属性またはビュー属性。 `layer=comp`の場合は、現在の画層または最終ビュー画像に適用されます。 エフェクトレイヤでは無視されます。

## 初期設定 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` アンシャープマスク効果がない。

## 関連項目 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) ,  [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)

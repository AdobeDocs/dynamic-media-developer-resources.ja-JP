---
title: op_usm
description: アンシャープマスク。 アンシャープは、layer=comp の場合、すべての拡大・縮小の後で、レイヤーまたは最終的なビュー画像をマスクします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 6%

---

# op_usm{#op-usm}

アンシャープマスク。 アンシャープは、layer=comp の場合、すべての拡大・縮小の後で、レイヤーまたは最終的なビュー画像をマスクします。

パラメータは、最大解像度の画像に適用されると想定され、ダウンサンプリングされた画像を処理する際に縮小されます。

`op_usm= *`量`*[, *`半径`*[, *`しきい値`*[, *`モノクロ`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 値</span></span> </p></td> 
  <td class="stentry"> <p>フィルタ強度係数（実数 0 ～ 5） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半径</span></span> </p></td> 
  <td class="stentry"> <p>フィルターカーネル半径（ピクセル単位、実数 0 ～ 250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> しきい値</span></span> </p></td> 
  <td class="stentry"> <p>フィルタしきい値レベル（整数 0 ～ 255）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> モノクロ</span></span> </p></td> 
  <td class="stentry"> <p>各カラーコンポーネントに個別に適用する場合は 0 に、画像の明るさ（強さ）にのみ適用する場合は 1 に設定します。 </p> <p> <span class="codeph"><span class="varname"> モノクロ</span></span> は、グレースケール画像では無視されます。 </p></td> 
 </tr> 
</table>

レイヤーマスクや合成マスクもシャープにされます。

## プロパティ {#section-fb5311b34d164946b74dadb32359518a}

画層属性またはビュー属性。 現在の画層に適用されます。 `layer=comp`. 効果画層で無視されます。

## 初期設定 {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usm=0,0,0,0` アンシャープマスク効果がないので。

## 関連項目 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)

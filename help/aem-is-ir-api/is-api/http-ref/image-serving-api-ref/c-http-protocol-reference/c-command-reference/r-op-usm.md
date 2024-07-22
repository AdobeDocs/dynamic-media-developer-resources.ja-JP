---
title: op_usm
description: アンシャープマスク。 アンシャープマスクは、レイヤー=comp の場合、すべての拡大縮小の後にレイヤーまたは最終ビューイメージをマスクします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 1%

---

# op_usm{#op-usm}

アンシャープマスク。 アンシャープマスクは、レイヤー=comp の場合、すべての拡大縮小の後にレイヤーまたは最終ビューイメージをマスクします。

このパラメーターは、フル解像度画像に適用されると想定され、ダウンサンプリングされた画像の処理時に縮小されます。

`op_usm= *`amount`*[, *`radius`*[, *`threshold`*[, *`monochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 額 </span></span> </p></td> 
  <td class="stentry"> <p>フィルター強度係数（実際の 0...5）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 半径 </span></span> </p></td> 
  <td class="stentry"> <p>フィルターカーネル半径（ピクセル単位）（実際の 0...250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> きい値 </span></span> </p></td> 
  <td class="stentry"> <p>フィルターしきい値（int 0...255）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>モノクロ <span class="codeph"><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>0 に設定すると各色成分に個別に適用され、1 に設定すると画像の明るさ（強さ）にのみ適用されます。 </p> <p> モノクロ <span class="codeph"><span class="varname"> は </span></span> グレースケール画像では無視されます。 </p></td> 
 </tr> 
</table>

レイヤーマスクまたはコンポジットマスクもシャープになります。

## プロパティ {#section-fb5311b34d164946b74dadb32359518a}

レイヤ アトリビュートまたはビューアトリビュート。 現在の画層、または `layer=comp` の場合は最終表示イメージに適用されます。 エフェクトレイヤーで無視されます。

## 初期設定 {#section-2bedc99866ff473e90e5ea36596d8362}

アンシャープマスク効果がない場合は `op_usm=0,0,0,0` を使用します。

## 関連項目 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)

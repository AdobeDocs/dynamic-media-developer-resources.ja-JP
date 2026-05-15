---
title: op_usm
description: アンシャープマスク。 レイヤー=コンポジションの場合、すべての拡大縮小の後に、レイヤーまたは最終的なビュー画像をアンシャープマスクします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a83d6326-9029-4c5c-a069-92bc81120866
TQID: 'https://experienceleague.adobe.com/Q2-9E1SNDgr8rGYWNKDLlVcQU85EhpEXhxAqF3WrJic'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 1%

---

# op_usm{#op-usm}

アンシャープマスク。 レイヤー=コンポジションの場合、すべての拡大縮小の後に、レイヤーまたは最終的なビュー画像をアンシャープマスクします。

パラメーターは、フル解像度の画像に適用されると想定され、ダウンサンプルされた画像を処理する際に縮小されます。

`op_usm= *`amount`*[, *`radius`*[, *`threshold`*[, *`monochrome`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">金額</span></span> </p></td> 
  <td class="stentry"> <p>フィルター強度係数（実数0...5） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">半径</span></span> </p></td> 
  <td class="stentry"> <p>カーネルの半径をピクセル単位でフィルタリングします（実数0 ～ 250）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">しきい値</span></span> </p></td> 
  <td class="stentry"> <p>フィルターしきい値レベル （int 0...255）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> モノクロ </span></span> </p></td> 
  <td class="stentry"> <p>各カラーコンポーネントに個別に適用する場合は0に、画像の明るさ（強度）のみに適用する場合は1に設定します。 </p> <p> グレースケール画像では、<span class="codeph"><span class="varname"> モノクロ </span></span>は無視されます。 </p></td> 
 </tr> 
</table>

レイヤーマスクまたは複合マスクもシャープになります。

## プロパティ {#section-fb5311b34d164946b74dadb32359518a}

レイヤー属性またはビュー属性。 現在のレイヤーまたは`layer=comp`の場合は最終的なビュー画像に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-2bedc99866ff473e90e5ea36596d8362}

アンシャープマスク効果のない`op_usm=0,0,0,0`。

## 関連項目 {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)、[op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)、[op_usmR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usmr.md#reference-c0168bc1e3a24370883670c09bcb0fef)

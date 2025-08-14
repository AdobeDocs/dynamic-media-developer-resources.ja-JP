---
title: op_growMaskR
description: 画像を拡大/侵食します。 マスク データに形態学的拡張（半径 > 0）または侵食（半径 < 0）を適用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# op_growMaskR{#op-growmaskr}

画像を拡大/侵食します。 マスク データに形態学的拡張（半径 > 0）または侵食（半径 &lt; 0）を適用します。

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>マスクがダウンサンプリングされるかどうか（整数–100..100）に関係なく、<span class="codeph"><span class="varname"> 半径 R</span></span> が適用されるピクセル単位の半径を拡張/侵食します。 </p></td> 
 </tr> 
</table>

主に、マスクのエッジ周辺のアーティファクトを避けるために、マスクを少し拡大または縮小するために使用します。

## プロパティ {#section-b1c66d65168d4ea695e8662ea690bd4e}

現在の画層、または `0` の場合は画層 `layer=comp` に適用されます。

## 初期設定 {#section-14c908bb87cb42acbea709effea2f964}

変 `op_growMaskR=0` なく構いません。

## 関連項目 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[レイヤー効果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)

---
title: op_growMaskR
description: 画像をディレート/エローディングします。 マスクデータに形態学的な拡張（半径> 0）または侵食（半径< 0）を適用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
TQID: 'https://experienceleague.adobe.com/tMIQ-hwgc0cegbHk0hdHI0MGgdXkXqyiFexEVKkEiPI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 3%

---

# op_growMaskR{#op-growmaskr}

画像をディレート/エローディングします。 マスクデータに形態学的な拡張（半径> 0）または侵食（半径&lt; 0）を適用します。

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>マスクがダウンサンプルされているかどうかに関係なく、<span class="codeph"><span class="varname">半径R</span></span>がそのまま適用されるピクセル単位で半径を拡大/縮小します（int -100..100）。 </p></td> 
 </tr> 
</table>

主に、マスクのエッジの周りのアーティファクトを避けるために、マスクをわずかに拡大または縮小するために使用されます。

## プロパティ {#section-b1c66d65168d4ea695e8662ea690bd4e}

現在のレイヤーまたは`layer=comp`の場合はレイヤー`0`に適用されます。

## 初期設定 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`、変更なし。

## 関連項目 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[レイヤー効果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)

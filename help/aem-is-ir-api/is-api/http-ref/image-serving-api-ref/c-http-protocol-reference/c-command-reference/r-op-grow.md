---
title: op_grow
description: 画像をディレート/エローディングします。 画像データに形態学的な拡張（半径> 0）または侵食（半径< 0）を適用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
TQID: 'https://experienceleague.adobe.com/vNFqqzcSqktgB5ohUZjqf0RtQNOD-t7fxITR2gZl-T4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 2%

---

# op_grow{#op-grow}

画像をディレート/エローディングします。 画像データに形態学的な拡張（半径> 0）または侵食（半径&lt; 0）を適用します。

`op_grow= *`半径`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">半径</span></span> </p> </td> 
  <td class="stentry"> <p>半径をピクセル単位で拡大/縮小（int -100..100） </p></td> 
 </tr> 
</table>

`*`半径`*`は、合成画像に対するピクセル単位です。 画像がカラーの場合、各コンポーネントは独立して処理されます。

主にレイヤー効果のサイズを変更するために使用されます。 マスクを使用してテキストレイヤーまたは単色レイヤーに特殊効果を適用する場合にも便利です。

## プロパティ {#section-b1c66d65168d4ea695e8662ea690bd4e}

レイヤー属性。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。

## 初期設定 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`、変更なし。

## 関連項目 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[レイヤー効果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

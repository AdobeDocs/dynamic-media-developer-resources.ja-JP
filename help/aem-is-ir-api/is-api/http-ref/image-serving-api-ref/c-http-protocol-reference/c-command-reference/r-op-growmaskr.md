---
description: 画像をディレート/エロードします。 形態素ディレート（半径> 0）または侵食（半径< 0）をマスクデータに適用します。
seo-description: 画像をディレート/エロードします。 形態素ディレート（半径> 0）または侵食（半径< 0）をマスクデータに適用します。
seo-title: op_growMaskR
solution: Experience Manager
title: op_growMaskR
topic: Scene7 Image Serving - Image Rendering API
uuid: b81968e7-ebaf-426c-9230-1afcf4b5cf24
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# op_growMaskR{#op-growmaskr}

画像をディレート/エロードします。 形態素ディレート（半径> 0）または侵食（半径&lt; 0）をマスクデータに適用します。

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>マスクがダウンサンプルされているかどうかに関係なく、<span class="codeph"><span class="varname"> radiusR</span></span>がそのまま適用されるピクセル単位のディレート/エロード半径（整数 —100 ～ 100）。 </p></td> 
 </tr> 
</table>

主に、マスクのエッジの周囲に生じるアーチファクトを回避するために、マスクを少し拡大または縮小するために使用します。

## プロパティ {#section-b1c66d65168d4ea695e8662ea690bd4e}

現在の画層に適用されます。または、`layer=comp`の場合は画層`0`に適用されます。

## 初期設定 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`（変更なし）。

## 関連項目 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[レイヤー効果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)

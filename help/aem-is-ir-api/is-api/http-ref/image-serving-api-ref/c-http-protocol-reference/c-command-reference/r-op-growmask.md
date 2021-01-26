---
description: 画像をディレート/エロードします。 形態素ディレート（半径> 0）または侵食（半径< 0）をマスクデータに適用します。
seo-description: 画像をディレート/エロードします。 形態素ディレート（半径> 0）または侵食（半径< 0）をマスクデータに適用します。
seo-title: op_growMask
solution: Experience Manager
title: op_growMask
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 016501e8-33c5-4c9e-8d26-120b1e929c55
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# op_growMask{#op-growmask}

画像をディレート/エロードします。 形態素ディレート（半径> 0）または侵食（半径&lt; 0）をマスクデータに適用します。

`op_growMask= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>半径が最大解像度マスクに適用されると想定されるピクセル単位の拡大/縮小半径です。したがって、ダウンサンプルマスク（整数 —100 ～ 100）の場合は縮小されます。 </p></td> 
 </tr> 
</table>

主に、マスクのエッジの周囲に生じるアーチファクトを回避するために、マスクを少し拡大または縮小するために使用します。

## プロパティ {#section-b1c66d65168d4ea695e8662ea690bd4e}

現在の画層に適用されます。または、`layer=comp`の場合は画層`0`に適用されます。

## 初期設定 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`（変更なし）。

## 関連項目 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[レイヤー効果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)

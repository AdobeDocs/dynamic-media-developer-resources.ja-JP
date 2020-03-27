---
description: 画像をディレート/侵食します。 形態学的なディレート（半径> 0）または侵食（半径< 0）をマスクデータに適用します。
seo-description: 画像をディレート/侵食します。 形態学的なディレート（半径> 0）または侵食（半径< 0）をマスクデータに適用します。
seo-title: op_growMask
solution: Experience Manager
title: op_growMask
topic: Scene7 Image Serving - Image Rendering API
uuid: 016501e8-33c5-4c9e-8d26-120b1e929c55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_growMask{#op-growmask}

画像をディレート/侵食します。 形態学的なディレート（半径> 0）または侵食（半径&lt; 0）をマスクデータに適用します。

`op_growMask= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>半径の拡大/縮小（ピクセル単位）。radiusは最大解像度マスクに適用されると想定され、ダウンサンプルマスクの場合は縮小されます（整数 —100 ～ 100）。 </p></td> 
 </tr> 
</table>

主に、マスクの端の周りに生じるアーチファクトを避けるために、マスクを少し拡大または縮小する目的で使用します。

## プロパティ {#section-b1c66d65168d4ea695e8662ea690bd4e}

現在のレイヤーまたはレイヤー（の場合）に適 `0` 用されま `layer=comp`す。

## 初期設定 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`（変更なし）。

## 関連項目 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[レイヤー効果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)

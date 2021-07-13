---
description: 画像を拡大/縮小します。 マスクデータに形態素ディレート（半径> 0）またはエローデ（半径< 0）を適用します。
solution: Experience Manager
title: op_growMask
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---

# op_growMask{#op-growmask}

画像を拡大/縮小します。 マスクデータに形態素ディレート（半径> 0）またはエローデ（半径&lt; 0）を適用します。

`op_growMask= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>半径が最大解像度マスクに適用されると想定されるピクセル単位のディレート/エロード半径。したがって、ダウンサンプリングされたマスク（整数 —100 ～ 100）に対して縮小されます。 </p></td> 
 </tr> 
</table>

主に、マスクのエッジの周囲にアーティファクトを避けるために、マスクをわずかに拡大または縮小するために使用します。

## プロパティ {#section-b1c66d65168d4ea695e8662ea690bd4e}

現在の画層に適用されます。 `layer=comp`の場合は画層`0`に適用されます。

## 初期設定 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`（変更なし）。

## 関連項目 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[レイヤー効果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)

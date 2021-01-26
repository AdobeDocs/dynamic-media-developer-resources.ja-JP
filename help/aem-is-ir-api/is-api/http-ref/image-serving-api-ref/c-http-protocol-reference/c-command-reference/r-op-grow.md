---
description: 画像をディレート/エロードします。 画像データに形態素ディレート（半径> 0）または浸食（半径< 0）を適用します。
seo-description: 画像をディレート/エロードします。 画像データに形態素ディレート（半径> 0）または浸食（半径< 0）を適用します。
seo-title: op_grow
solution: Experience Manager
title: op_grow
topic: Dynamic Media Image Serving - Image Rendering API
uuid: bc9bf889-f7e1-4a65-b6d6-7e1257ef8c11
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# op_grow{#op-grow}

画像をディレート/エロードします。 画像データに形態素ディレート（半径> 0）または浸食（半径&lt; 0）を適用します。

`op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>半径（整数 —100 ～ 100）をピクセル単位で表します。 </p></td> 
 </tr> 
</table>

`*`合成画像を基準としたピクセル単位の`*` 半径。画像がカラーの場合、各コンポーネントは独立して処理されます。

主に、レイヤー効果のサイズを変更するために使用します。 また、テキストレイヤーやマスク付きべた塗りレイヤーに特殊効果を適用する場合にも便利です。

## プロパティ {#section-b1c66d65168d4ea695e8662ea690bd4e}

レイヤー属性。 `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。

## 初期設定 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`（変更なし）。

## 関連項目 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[レイヤー効果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

---
description: 画像を拡大/縮小します。 画像データに形態素ディレート（半径> 0）またはエローデ（半径< 0）を適用します。
solution: Experience Manager
title: op_grow
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---

# op_grow{#op-grow}

画像を拡大/縮小します。 画像データに形態素ディレート（半径> 0）またはエローデ（半径&lt; 0）を適用します。

`op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>半径をピクセル単位（整数 —100 ～ 100）で表示します。 </p></td> 
 </tr> 
</table>

`*``*` 合成画像を基準とするピクセル単位の半径。画像がカラーの場合、各コンポーネントは個別に処理されます。

主に、レイヤー効果のサイズを変更するために使用します。 また、テキストレイヤーやマスク付きのソリッドカラーレイヤーに特殊効果を適用する場合にも便利です。

## プロパティ {#section-b1c66d65168d4ea695e8662ea690bd4e}

レイヤー属性。 `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。

## 初期設定 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`（変更なし）。

## 関連項目 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[レイヤー効果](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

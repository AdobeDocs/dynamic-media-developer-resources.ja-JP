---
title: qlt
description: JPEG 画質。 JPEGレベルを制御するための圧縮エンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）が変わり、間接的には結果の画像の画質も変わります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 15%

---

# qlt{#qlt}

JPEG 画質。 JPEGレベルを制御するための圧縮エンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）が変わり、間接的には結果の画像の画質も変わります。

` qlt= *` 品質 `*[, *` 彩度 `*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> quality </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディングの品質（1...100 整数）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> chroma </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEGの色度のダウンサンプリング （0 =標準、1 =無効）。オプション。デフォルトは 0 です。 </p> </td> 
 </tr> 
</table>

`fmt=jpg` の場合にのみ使用されます。 それ以外は無視

大きな値を指定すると高画質になりますがファイルサイズが大きくなり、小さな値を指定するとファイルサイズが抑えられますが見た目の画質が低下します。90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

一般的なJPEGエンコーダで使用されるRGB色度ダウンサンプリングを無効にするには、`chroma` フラグを設定します。 これにより、画像のエッジが明るさではなく色合いの変化で定義されている場合、エッジの鮮明さが増す可能性があります。 このフラグを設定すると、ファイルサイズがわずかに大きくなる場合があります。 テキストが少しぼやけて見える場合は、この設定を試してください。

出力ピクセルタイプが CMYK またはグレーの場合、`chroma` は無視されます。

## 例 {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`

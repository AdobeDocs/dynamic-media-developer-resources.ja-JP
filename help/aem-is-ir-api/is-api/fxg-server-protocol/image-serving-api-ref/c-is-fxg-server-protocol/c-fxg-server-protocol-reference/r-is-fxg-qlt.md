---
title: qlt
description: JPEG 画質。 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、結果の画像のファイルサイズ（返信データの量）と、間接的に生成される画像の視覚的な品質が変化します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 15%

---

# qlt{#qlt}

JPEG 画質。 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、結果の画像のファイルサイズ（返信データの量）と、間接的に生成される画像の視覚的な品質が変化します。

` qlt= *`品質`*[, *`色度`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 品質 </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディング品質 (1 ～ 100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色度 </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度のダウンサンプリング（0=通常、1=無効）。オプション。デフォルトは 0 です。 </p> </td> 
 </tr> 
</table>

次の場合にのみ使用されます。 `fmt=jpg`. それ以外の場合は無視

大きな値を指定すると高画質になりますがファイルサイズが大きくなり、小さな値を指定するとファイルサイズが抑えられますが見た目の画質が低下します。90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

を設定します。 `chroma` フラグを使用して、一般的なRGBエンコーダーで使用するJPEG色度のダウンサンプリングを無効にします。 これにより、明るさではなく色相の変化によってエッジが定義された場合に、イメージ内のエッジの鮮明さが増す場合があります。 このフラグを設定すると、ファイルサイズが少し大きくなる場合があります。 テキストが少しぼやけて見える場合は、この設定を試してください。

The `chroma` 出力ピクセルの種類が CMYK またはグレーの場合、は無視されます。

## 例 {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`

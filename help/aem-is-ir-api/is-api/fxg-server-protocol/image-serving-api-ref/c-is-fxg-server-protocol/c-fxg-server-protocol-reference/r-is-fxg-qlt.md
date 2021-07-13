---
description: JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、結果の画像のファイルサイズ（応答データの量）と、間接的に生成される画像の画質が変わります。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 15%

---

# qlt{#qlt}

JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、結果の画像のファイルサイズ（応答データの量）と、間接的に生成される画像の画質が変わります。

` qlt= *``*[, *`画質`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 品質  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディング品質(1 ～ 100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色度  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度のダウンサンプリング（0=通常、1=無効）オプション。デフォルトは0です。 </p> </td> 
 </tr> 
</table>

`fmt=jpg`の場合にのみ使用されます。 それ以外の場合は無視

大きな値を指定すると高画質になりますがファイルサイズが大きくなり、小さな値を指定するとファイルサイズが抑えられますが見た目の画質が低下します。90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

`chroma`フラグを設定して、一般的なJPEGエンコーダーで使用されるRGB色度のダウンサンプリングを無効にします。 これにより、明るさではなく色相の変化によってエッジが定義された場合に、イメージ内のエッジの鮮明さが増す場合があります。 このフラグを設定すると、ファイルサイズが少し大きくなる場合があります。 テキストが少しぼやけて表示される場合は、この設定を試してみてください。

`chroma` 出力ピクセルタイプがCMYKまたはグレーの場合、は無視されます。

## 例 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]

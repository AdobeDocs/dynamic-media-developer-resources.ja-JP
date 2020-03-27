---
description: JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）や、間接的に、結果の画像の画質が変化します。
seo-description: JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）や、間接的に、結果の画像の画質が変化します。
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）や、間接的に、結果の画像の画質が変化します。

` qlt= *`色`*[, *`質`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 質 </span></span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディング品質(1 ～ 100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色 </span> 素 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度ダウンサンプリング（0=通常、1=無効）;オプションです。初期設定は0です。 </p> </td> 
 </tr> 
</table>

次の場合にのみ使用されま `fmt=jpg`す。 それ以外は無視

大きな値を指定すると高画質になりますがファイルサイズが大きくなり、小さな値を指定するとファイルサイズが抑えられますが見た目の画質が低下します。90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

標準的なJPEGエン `chroma` コーダーで使用されるRGB色度のダウンサンプリングを無効にするには、このフラグを設定します。 これにより、明るさではなく色相の変化によってエッジが定義される場合に、画像のエッジの知覚的なシャープさが増す可能性があります。 このフラグを設定すると、ファイルサイズが少し大きくなる場合があります。 テキストが少しぼやけて表示される場合は、この設定を試してみてください。

`chroma` は、出力ピクセルの種類がCMYKまたはグレーの場合は無視されます。

## 例 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]

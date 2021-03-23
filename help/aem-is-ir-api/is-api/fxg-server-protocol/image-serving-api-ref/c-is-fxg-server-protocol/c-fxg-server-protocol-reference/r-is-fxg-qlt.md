---
description: JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）や間接的に、生成される画像の画質が変化します。
seo-description: JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）や間接的に、生成される画像の画質が変化します。
seo-title: qlt
solution: Experience Manager
title: qlt
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 12%

---


# qlt{#qlt}

JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）や間接的に、生成される画像の画質が変化します。

` qlt= *``*[, *`色質`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 品質  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディング画質(1 ～ 100 int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色素  </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度ダウンサンプリング（0 =標準、1 =無効）;オプションです。初期設定は0です。 </p> </td> 
 </tr> 
</table>

`fmt=jpg`の場合にのみ使用されます。 それ以外は無視

大きな値を指定すると高画質になりますがファイルサイズが大きくなり、小さな値を指定するとファイルサイズが抑えられますが見た目の画質が低下します。90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

`chroma`フラグを設定して、一般的なJPEGエンコーダーで使用されるRGB色度ダウンサンプリングを無効にします。 これにより、明るさではなく色相の変化によってエッジが定義された場合に、画像内のエッジの鋭さが増す可能性があります。 このフラグを設定すると、ファイルサイズが少し大きくなる場合があります。 テキストが少しぼやけて表示される場合は、この設定を試してみてください。

`chroma` は、出力ピクセルの種類がCMYKまたはグレーの場合は無視されます。

## 例 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]

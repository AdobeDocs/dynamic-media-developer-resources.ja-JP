---
title: qlt
description: Jpeg品質： 圧縮レベルを制御するためのJPEG エンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）、および間接的に結果の画像の視覚的品質が変化します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
TQID: 'https://experienceleague.adobe.com/sf3ydtf3lGCG1BfJfc1vW5hXFBawbeWJwXNSJdUEei8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 15%

---

# qlt{#qlt}

Jpeg品質： 圧縮レベルを制御するためのJPEG エンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）、および間接的に結果の画像の視覚的品質が変化します。

` qlt= *`品質`*[, *` クロマ `*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">品質</span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG エンコーディングの品質（1...100 int）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> クロマ </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEGの色度ダウンサンプリング（0=標準、1=無効）。オプション、デフォルトは0です。 </p> </td> 
 </tr> 
</table>

`fmt=jpg`の場合にのみ使用されます。 それ以外は無視

大きな値を指定すると高画質になりますがファイルサイズが大きくなり、小さな値を指定するとファイルサイズが抑えられますが見た目の画質が低下します。 90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

`chroma` フラグを設定して、一般的なJPEG エンコーダで使用されるRGB色度のダウンサンプリングを無効にします。 これにより、エッジが明るさではなく色相の変化によって定義される場合、画像内のエッジの知覚的鮮明さが増加する可能性があります。 このフラグを設定すると、ファイルサイズが若干増加する場合があります。 テキストが少しぼやけている場合は、この設定を試してください。

出力ピクセルタイプがCMYKまたはグレーの場合、`chroma`は無視されます。

## 例 {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`

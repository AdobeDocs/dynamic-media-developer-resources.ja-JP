---
title: qlt
description: JPEG 画質。 圧縮レベルを制御するJPEGエンコーディング属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 7%

---

# qlt{#qlt}

JPEG 画質。 圧縮レベルを制御するJPEGエンコーディング属性を指定します。

` qlt= *`品質`*[. *`色度`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 質 </span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディングの品質 (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度のダウンサンプリング（0=通常、1=無効）オプションです。デフォルトは 0 です。 </p> </td> 
 </tr> 
</table>

圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、結果のイメージのファイルサイズ（返信データの量）と、間接的に生成されるイメージの視覚的な品質が変化します。

高 *`quality`* 値を指定すると、ファイルのサイズと画質が高くなり、値を小さくするとファイルのサイズが小さくなり、知覚される画質が低下します。 90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

を *`chroma`* フラグを使用して、一般的なJPEGエンコーダーで使用される色度のダウンサンプリングを無効にします。 この設定により、明るさではなく色相の変化によってエッジが定義された場合に、イメージ内のエッジの鮮明さが増す場合があります。 このフラグを設定すると、ファイルサイズが少し大きくなる場合があります。 テキストが少しぼやけて見える場合は、この設定を試してください。

## プロパティ {#section-897b61c786dd4230a2c5807f2f40e722}

リクエストの任意の場所で発生する場合があります。

出力画像形式が圧縮をサポートしていない場合は無視され、JPEGを圧縮します。 詳しくは、 `fmt=` を参照してください。

## 初期設定 {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## 関連項目 {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)

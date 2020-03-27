---
description: JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。
seo-description: JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 46f5b0da-7fe7-4daf-947b-bb5f5f5f5e6d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。

` qlt= *`色`*[. *`質`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 質 </span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディング画質(1 ～ 100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度ダウンサンプリング（0=通常、1=無効）;オプションです。初期設定は0です。 </p> </td> 
 </tr> 
</table>

圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）や、間接的に、結果の画像の画質が変化します。

Higher *`quality`* values increase file size and quality, lower values decrease file sizes and reduce perceived image quality. 90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

標準的なJPEGエン *`chroma`* コーダーで使用される色度のダウンサンプリングを無効にするには、フラグを設定します。 これにより、明るさではなく色相の変化によってエッジが定義される場合に、画像のエッジの知覚的なシャープさが増す可能性があります。 このフラグを設定すると、ファイルサイズが少し大きくなる場合があります。 テキストが少しぼやけて表示される場合は、この設定を試してみてください。

## プロパティ {#section-897b61c786dd4230a2c5807f2f40e722}

リクエストの任意の場所で発生する可能性があります。

出力画像形式がJPEG圧縮をサポートしていない場合は無視されます。 JPEG圧縮をサポートする出力 `fmt=` 画像形式のリストについては、の説明を参照してください。

## 初期設定 {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## 関連項目 {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)

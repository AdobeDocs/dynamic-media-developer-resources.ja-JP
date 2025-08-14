---
title: qlt
description: JPEG 画質。 圧縮レベルを制御するためのJPEG エンコーディング属性を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 7%

---

# qlt{#qlt}

JPEG 画質。 圧縮レベルを制御するためのJPEG エンコーディング属性を指定します。

` qlt= *` 品質 `*[. *` 彩度 `*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> quality </span> </p> </td> 
  <td class="stentry"> <p>JPEGのエンコーディング品質（1...100） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>JPEGの色度ダウンサンプリング （0 =標準、1 =無効）。オプション。デフォルトは 0 です。 </p> </td> 
 </tr> 
</table>

圧縮レベルを制御するためのJPEG エンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）が変わり、間接的には結果の画像の画質も変わります。

*`quality`* の値を大きくすると、ファイルサイズが大きくなり、画質が向上します。値を小さくすると、ファイルサイズが小さくなり、画質が低下します。 90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

*`chroma`* フラグを設定して、一般的なJPEG エンコーダで使用される色度ダウンサンプリングを無効にします。 この設定により、画像のエッジが明るさではなく色合いの変化で定義されている場合、エッジの鮮明さが増す可能性があります。 このフラグを設定すると、ファイルサイズがわずかに大きくなる場合があります。 テキストが少しぼやけて見える場合は、この設定を試してください。

## プロパティ {#section-897b61c786dd4230a2c5807f2f40e722}

は、リクエスト内のどこでも発生する可能性があります。

出力画像の形式がJPEG圧縮をサポートしていない場合は無視されます。 JPEG圧縮をサポートする出力画像フォーマットのリストについては、`fmt=` の説明を参照してください。

## 初期設定 {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## 関連項目 {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)

---
title: qlt
description: JPEGの質。 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、結果の画像のファイルサイズ（返信データの量）と、間接的に生成される画像の視覚的な品質が変化します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 6%

---

# qlt{#qlt}

JPEGの質。 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、結果の画像のファイルサイズ（返信データの量）と、間接的に生成される画像の視覚的な品質が変化します。

` qlt= *`品質`*[, *`色度`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 質 </span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディング品質 (1 ～ 100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度のダウンサンプリング（0=通常、1=無効）。オプション。デフォルトは 0 です。 </p> </td> 
 </tr> 
</table>

高い *`quality`* 値を指定すると、ファイルのサイズと品質が高くなり、値を小さくすると、ファイルのサイズが小さくなり、知覚される画質が低下します。 90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

を設定します。 *`chroma`* フラグを使用して、一般的なRGBエンコーダーで使用するJPEG色度のダウンサンプリングを無効にします。 これにより、明るさではなく色相の変化によってエッジが定義された場合に、イメージ内のエッジの鮮明さが増す場合があります。 このフラグを設定すると、ファイルサイズが少し大きくなる場合があります。 テキストが少しぼやけて見える場合は、この設定を試してください。

## プロパティ {#section-925a44cbdc9042db8d4eb149cd073d21}

要求属性。 現在の画層設定に関係なく適用されます。 出力画像ファイル形式が画像のエンコーディングをサポートしていない場合はJPEGされません。 詳しくは、 `fmt=` ：どの出力画像形式がサポートされているかを示します。 `qlt=`.

*`chroma`* 出力ピクセルの種類が CMYK またはグレーの場合、は無視されます。

## 初期設定 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 例 {#section-d7d33871d401433aa51d028823eae7a9}

低帯域幅接続での伝送を高速化するために、品質を低下させます。

`http://server/myRoodId/myImageId?qlt=60&wid=300`

高帯域幅接続の品質を向上：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 関連項目 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)

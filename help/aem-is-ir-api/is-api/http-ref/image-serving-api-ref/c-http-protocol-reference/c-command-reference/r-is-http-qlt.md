---
description: JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）や、間接的に、結果の画像の画質が変化します。
seo-description: JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）や、間接的に、結果の画像の画質が変化します。
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f69845d-3b25-41a7-b6c0-83cf1d2bc450
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）や、間接的に、結果の画像の画質が変化します。

` qlt= *`色`*[, *`質`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 質 </span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディング品質(1 ～ 100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度ダウンサンプリング（0=通常、1=無効）;オプションです。初期設定は0です。 </p> </td> 
 </tr> 
</table>

Higher *`quality`* values increase file size and quality, lower values decrease file sizes and reduce perceived image quality. 90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

標準的なJPEGエン *`chroma`* コーダーで使用されるRGB色度のダウンサンプリングを無効にするには、このフラグを設定します。 これにより、明るさではなく色相の変化によってエッジが定義される場合に、画像のエッジの知覚的なシャープさが増す可能性があります。 このフラグを設定すると、ファイルサイズが少し大きくなる場合があります。 テキストが少しぼやけて表示される場合は、この設定を試してみてください。

## プロパティ {#section-925a44cbdc9042db8d4eb149cd073d21}

リクエスト属性。 現在のレイヤー設定に関係なく適用されます。 出力画像ファイル形式がJPEGエンコーディングをサポートしていない場合は無視されます。 どの出力画像形式がサポートさ `fmt=` れているかについては、の説明を参照してくださ `qlt=`い。

*`chroma`* は、出力ピクセルの種類がCMYKまたはグレーの場合は無視されます。

## 初期設定 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 例 {#section-d7d33871d401433aa51d028823eae7a9}

低帯域幅接続での伝送を高速化するため、品質を下げます。

`http://server/myRoodId/myImageId?qlt=60&wid=300`

高帯域幅接続の品質を向上：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 関連項目 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)

---
title: qlt
description: JPEG品質。 JPEGレベルを制御するための圧縮エンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）が変わり、間接的には結果の画像の画質も変わります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 6%

---

# qlt{#qlt}

JPEG品質。 JPEGレベルを制御するための圧縮エンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）が変わり、間接的には結果の画像の画質も変わります。

` qlt= *` 品質 `*[, *` 彩度 `*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> quality </span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディングの品質（1...100 整数）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>JPEGの色度のダウンサンプリング （0 =標準、1 =無効）。オプション。デフォルトは 0 です。 </p> </td> 
 </tr> 
</table>

*`quality`* の値を大きくすると、ファイルサイズが大きくなり、画質が向上します。値を小さくすると、ファイルサイズが小さくなり、画質が低下します。 90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

一般的なJPEGエンコーダで使用されるRGB色度ダウンサンプリングを無効にするには、*`chroma`* フラグを設定します。 これにより、画像のエッジが明るさではなく色合いの変化で定義されている場合、エッジの鮮明さが増す可能性があります。 このフラグを設定すると、ファイルサイズがわずかに大きくなる場合があります。 テキストが少しぼやけて見える場合は、この設定を試してください。

## プロパティ {#section-925a44cbdc9042db8d4eb149cd073d21}

リクエスト属性。 現在のレイヤ設定に関係なく適用されます。 出力画像ファイル形式がJPEGエンコーディングをサポートしていない場合は無視されます。 サポートされている出力画像形式については、`fmt=` の説明を参照してくだ `qlt=` い。

出力ピクセルタイプが CMYK またはグレーの場合、*`chroma`* は無視されます。

## 初期設定 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 例 {#section-d7d33871d401433aa51d028823eae7a9}

低帯域幅接続で高速に送信するために品質を下げる：

`http://server/myRoodId/myImageId?qlt=60&wid=300`

高帯域幅接続の品質の向上：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 関連項目 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)

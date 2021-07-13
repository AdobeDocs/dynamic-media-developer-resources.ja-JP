---
description: JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、結果の画像のファイルサイズ（応答データの量）と、間接的に生成される画像の画質が変わります。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 6%

---

# qlt{#qlt}

JPEG画質 圧縮レベルを制御するJPEGエンコーディング属性を指定します。 これにより、結果の画像のファイルサイズ（応答データの量）と、間接的に生成される画像の画質が変わります。

` qlt= *``*[, *`画質`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 質 </span> </p> </td> 
  <td class="stentry"> <p>JPEGエンコーディング品質(1 ～ 100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度  </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度のダウンサンプリング（0=通常、1=無効）オプション。デフォルトは0です。 </p> </td> 
 </tr> 
</table>

*`quality`*&#x200B;の値を大きくするとファイルサイズと画質が大きくなり、小さくするとファイルサイズが小さくなり、知覚される画質が小さくなります。 90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

*`chroma`*&#x200B;フラグを設定して、一般的なJPEGエンコーダーで使用されるRGB色度のダウンサンプリングを無効にします。 これにより、明るさではなく色相の変化によってエッジが定義された場合に、イメージ内のエッジの鮮明さが増す場合があります。 このフラグを設定すると、ファイルサイズが少し大きくなる場合があります。 テキストが少しぼやけて表示される場合は、この設定を試してみてください。

## プロパティ {#section-925a44cbdc9042db8d4eb149cd073d21}

リクエスト属性。 現在の画層設定に関係なく適用されます。 出力画像ファイル形式がJPEGエンコーディングをサポートしていない場合は無視されます。 `qlt=`をサポートする出力画像形式については、`fmt=`の説明を参照してください。

*`chroma`* 出力ピクセルタイプがCMYKまたはグレーの場合、は無視されます。

## 初期設定 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 例 {#section-d7d33871d401433aa51d028823eae7a9}

低帯域幅接続での伝送を高速化するための品質の低下：

`http://server/myRoodId/myImageId?qlt=60&wid=300`

高帯域幅接続の品質を向上：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 関連項目 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 、  [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)

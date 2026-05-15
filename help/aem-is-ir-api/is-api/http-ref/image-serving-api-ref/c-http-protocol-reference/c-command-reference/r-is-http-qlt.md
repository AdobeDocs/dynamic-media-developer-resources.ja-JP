---
title: qlt
description: JPEGの品質。 圧縮レベルを制御するためのJPEG エンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）、および間接的に結果の画像の視覚的品質が変化します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
TQID: 'https://experienceleague.adobe.com/e7zzYHSi7X5tdPAy-0CWTK-Wqs5nfhEDLs2HYJ1D-f4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 242
ht-degree: 6%

---

# qlt{#qlt}

JPEGの品質。 圧縮レベルを制御するためのJPEG エンコーディング属性を指定します。 これにより、ファイルサイズ（返信データの量）、および間接的に結果の画像の視覚的品質が変化します。

` qlt= *`品質`*[, *` クロマ `*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">品質</span> </p> </td> 
  <td class="stentry"> <p>JPEG エンコーディングの品質（1...100 int）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> クロマ </span> </p> </td> 
  <td class="stentry"> <p>JPEGの色度ダウンサンプリング（0=標準、1=無効）。オプション、デフォルトは0です。 </p> </td> 
 </tr> 
</table>

*`quality`*&#x200B;値を大きくすると、ファイルサイズと画質が大きくなり、値を小さくすると、ファイルサイズが小さくなり、画像の質が低下します。 90 を超える値を指定すると、一般的には非圧縮画像と区別がつかないほどの画像が生成されます。

*`chroma`* フラグを設定して、一般的なJPEG エンコーダで使用されるRGB色度のダウンサンプリングを無効にします。 これにより、エッジが明るさではなく色相の変化によって定義される場合、画像内のエッジの知覚的鮮明さが増加する可能性があります。 このフラグを設定すると、ファイルサイズが若干増加する場合があります。 テキストが少しぼやけている場合は、この設定を試してください。

## プロパティ {#section-925a44cbdc9042db8d4eb149cd073d21}

リクエスト属性： 現在のレイヤー設定に関係なく適用されます。 出力画像ファイル形式がJPEG エンコーディングをサポートしていない場合は無視されます。 出力画像形式が`qlt=`をサポートする詳細については、`fmt=`の説明を参照してください。

出力ピクセルタイプがCMYKまたはグレーの場合、*`chroma`*&#x200B;は無視されます。

## 初期設定 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 例 {#section-d7d33871d401433aa51d028823eae7a9}

低帯域幅の接続でより速い伝送のために品質を下げます：

`http://server/myRoodId/myImageId?qlt=60&wid=300`

高帯域幅の接続の品質を向上：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 関連項目 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)、[属性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)

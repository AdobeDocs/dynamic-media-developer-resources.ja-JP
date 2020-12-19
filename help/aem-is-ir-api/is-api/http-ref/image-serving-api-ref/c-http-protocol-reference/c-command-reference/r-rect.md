---
description: 最終的な表示の長方形。 最終的な表示画像を複数のストリップまたはタイルに分解できます。これらの画像は、端に沿ったアーティファクトを発生させず、個別に配信し、クライアントによってシームレスに再アセンブルできます。
seo-description: 最終的な表示の長方形。 最終的な表示画像を複数のストリップまたはタイルに分解できます。これらの画像は、端に沿ったアーティファクトを発生させず、個別に配信し、クライアントによってシームレスに再アセンブルできます。
seo-title: rect
solution: Experience Manager
title: rect
topic: Scene7 Image Serving - Image Rendering API
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# rect{#rect}

最終的な表示の長方形。 最終的な表示画像を複数のストリップまたはタイルに分解できます。これらの画像は、端に沿ったアーティファクトを発生させず、個別に配信し、クライアントによってシームレスに再アセンブルできます。

`rect= *``*, *``*[, *`脊索`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 共謀者</span> </p> </td> 
  <td class="stentry"> <p>表示画像の左上隅から表示の長方形の左上隅へのピクセルオフセット（整数、整数）。<span class="varname"> scale</span>が適用された後のピクセル単位で表します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> サイズ</span> </p></td> 
  <td class="stentry"> <p>ROIのサイズ（ピクセル単位、整数）。 返信画像のサイズを指定します。 表示画像の範囲外の領域の画像は<span class="codeph"> bgc=</span>で塗りつぶされます（リクエスト内に<span class="codeph"> fmt=*-alpha</span>が存在する場合は左に透明）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>尺度係数（実数） 1.0より小さい値を指定すると解像度が低くなり、1.0より大きい値を指定すると解像度が高くなります。 </p></td> 
 </tr> 
</table>

このコマンドを使用すると、画像サービングは大きい画像をHTTP経由で配信できます。そうしないと`attribute::MaxPix`で設定されたサイズ制限を超えます。

>[!NOTE]
>
>JPEG圧縮を使用する場合に最適な結果を得るには、ストリップまたはタイルのサイズは、JPEGエンコーディングのタイルサイズ（16 x 16ピクセル）の倍数にする必要があります。

## 例 {#section-932fcfcb41d74a29bc929e4430c49601}

印刷可能なCMYK画像を複数の最大解像度のストリップに分割して、ダウンロードファイルのサイズを小さくします。 連続した画像をリクエストする場合：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

まず、画像に関する関連情報を取得する。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

テキスト応答には、次のプロパティが含まれます。

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

この情報に基づいて、600 x 2000ピクセルのストリップを4つ必要とすることにしました。 `rect=`コマンドは、ストリップのサイズと位置を示すのに使用します。

このイメージは頻繁に変更されるので、CDNまたはプロキシサーバーにキャッシュされているイメージの古いバージョンから1つ以上のストリップが発生する可能性を最小限に抑えるために、`id=`コマンドを含めます。 `image.version`プロパティの値をこの目的に使用します。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## プロパティ {#section-aae223cee13e46d38b74680c048d945b}

表示属性。 現在のレイヤー設定に関係なく適用されます。

表示イメージの外側に広がるROIの領域はすべて`bgc=`で埋め込まれます。

重要な`rect=`は、`scl=`、`wid=`、`hei=`、`fit=`、`rgn=`、`align=`の最終的な拡大縮小と合わせの後に&#x200B;*適用されます。*

## 初期設定 {#section-b296d3bbfb19441f87137a452b70f19a}

変更されていない表示イメージ全体(`rect=0,0,width,height,1.0`)。

## 関連トピック {#section-74015202c0c545ec82aec614d74b4bbd}

[=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), wid= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)hei,  [hei, scl=, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)hei, scl=,  [hel=, hull=, hit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5) [, hit=, hgn, hit属性： max id=, max](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)

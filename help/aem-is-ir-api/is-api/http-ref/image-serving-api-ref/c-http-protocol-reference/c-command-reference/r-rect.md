---
title: rect
description: 最終ビューの長方形。 最終的なビューイメージを複数のストリップまたはタイルに分解できます。これらは、別々に配信し、クライアントがシームレスに再アセンブルでき、エッジに沿ったアーティファクトはありません。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 1%

---

# rect{#rect}

最終ビューの長方形。 最終的なビューイメージを複数のストリップまたはタイルに分解できます。これらは、別々に配信し、クライアントがシームレスに再アセンブルでき、エッジに沿ったアーティファクトはありません。

`rect= *`コード`*, *`サイズ`*[, *`スケール`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード</span> </p> </td> 
  <td class="stentry"> <p>表示画像の左上隅から表示長方形の左上隅（整数、整数）までのピクセルオフセット（ピクセル単位、後） <span class="varname"> スケール</span> が適用されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> サイズ</span> </p></td> 
  <td class="stentry"> <p>ROI のサイズ（ピクセル単位、整数）。 返信画像のサイズを指定します。 画像が <span class="codeph"> bgc=</span> ビュー画像で覆われていない領域 ( または透明のままの場合は <span class="codeph"> fmt=*-alpha</span> がリクエストに存在する )。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>尺度係数（実数） 1.0 より小さい値を指定すると解像度が低下し、1.0 より大きい値を指定すると解像度が高くなります。 </p></td> 
 </tr> 
</table>

画像サービングは、このコマンドを使用して、HTTP 経由で大きな画像を配信できます。このコマンドを使用すると、 `attribute::MaxPix`.

>[!NOTE]
>
>JPEG圧縮を使用する場合に最適な結果を得るには、ストリップまたはタイルのサイズは、JPEGエンコーディングタイルのサイズ（16 x 16 ピクセル）の倍数にする必要があります。

## 例 {#section-932fcfcb41d74a29bc929e4430c49601}

印刷可能な CMYK 画像を複数のフル解像度のストリップに分割して、ダウンロードファイルのサイズを小さくします。 連続した画像をリクエストする場合：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

まず、画像に関する関連情報を取得します。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

テキスト応答には、次のプロパティが含まれます。

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

この情報に基づいて、600 x 2000 ピクセルのストリップを 4 つ用意することにしました。 The `rect=` コマンドは、ストリップのサイズと位置を記述するために使用されます。

この画像は頻繁に変更されるので、 `id=` コマンドを使用して、CDN またはプロキシサーバーにキャッシュされた可能性のある古いバージョンの画像から、1 つ以上のストリップが発生する可能性を最小限に抑えることができます。 の値 `image.version` プロパティがこの目的で使用されます。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## プロパティ {#section-aae223cee13e46d38b74680c048d945b}

属性を表示します。 現在の画層設定に関係なく適用されます。

ビュー画像の外側に広がる ROI の領域は、 `bgc=`.

重要 `rect=` が適用されている *次より後* 最終的なスケーリングと～との適合 `scl=`, `wid=`, `hei=`, `fit=`, `rgn=`、および `align=`.

## 初期設定 {#section-b296d3bbfb19441f87137a452b70f19a}

ビュー画像全体、未変更 ( `rect=0,0,width,height,1.0`) をクリックします。

## 関連トピック {#section-74015202c0c545ec82aec614d74b4bbd}

[切り抜き=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)

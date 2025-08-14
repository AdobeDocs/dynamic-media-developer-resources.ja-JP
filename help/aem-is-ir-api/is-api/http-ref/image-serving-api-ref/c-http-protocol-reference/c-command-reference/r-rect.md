---
title: rect
description: 最終表示長方形 最終的なビュー画像を複数のストリップまたはタイルに分割でき、クライアントがシームレスに配信して再構築できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 1%

---

# rect{#rect}

最終表示長方形 最終的なビュー画像を複数のストリップまたはタイルに分割でき、クライアントがシームレスに配信して再構築できます。

`rect= *`coord`*, *`size`*[, *`scale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>ビューイメージの左上隅からビューの長方形の左上までのピクセル オフセット（int、int）が、<span class="varname"> の尺度の適用後にピクセル単位で表され </span> す。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> サイズ </span> </p></td> 
  <td class="stentry"> <p>ROI のサイズ （ピクセル単位） （整数、整数）。 返信画像のサイズを指定します。 画像は、ビュー画像で覆われていない領域（またはリクエストに fmt=*-alpha<span class="codeph"> が存在 </span> る場合は透明な領域）に <span class="codeph"> bgc=</span> で埋められます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> スケール </span> </p></td> 
  <td class="stentry"> <p>尺度係数（実数） 1.0 より小さい値を指定すると解像度が下がり、1.0 より大きい値を指定すると解像度が上がります。 </p></td> 
 </tr> 
</table>

このコマンドを使用すると、画像サービングは、HTTP 経由で大きな画像を配信できます。この HTTP が `attribute::MaxPix` で設定されたサイズ制限を超える場合があります。

>[!NOTE]
>
>最適な結果を得るには、JPEG圧縮を使用する場合、ストリップまたはタイルのサイズをJPEG エンコーディングタイルサイズ（16 x 16 ピクセル）の倍数にする必要があります。

## 例 {#section-932fcfcb41d74a29bc929e4430c49601}

印刷可能な CMYK 画像を複数のフル解像度のストリップに分割して、ダウンロードファイルのサイズを小さくします。 連続した画像をリクエストした場合：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

まず、画像に関する関連情報が取得されます。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

テキスト応答には、次のプロパティが含まれます。

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

この情報に基づいて、4 つの 600x2000 ピクセルストリップが望ましい。 `rect=` コマンドは、ストリップのサイズと位置を記述するために使用します。

このイメージは頻繁に変更されるため、`id=` のコマンドが含まれています。 これにより、CDN またはプロキシサーバーにキャッシュされている可能性のある古いバージョンの画像から 1 つ以上のストリップが残る可能性を最小限に抑えることができます。 `image.version` プロパティの値は、この目的で使用されます。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## プロパティ {#section-aae223cee13e46d38b74680c048d945b}

ビュー属性。 現在のレイヤ設定に関係なく適用されます。

ROI のうちビュー画像の外側に広がる領域には、`bgc=` が埋め込まれます。

`rect=`、*、*、`scl=`、`wid=` および `hei=` を使用した `fit=` 後 `rgn=` 最終的なスケーリングおよびフィッティングには、重要な `align=` が適用されます。

## 初期設定 {#section-b296d3bbfb19441f87137a452b70f19a}

変更されていないビュー画像全体（`rect=0,0,width,height,1.0`）。

## 関連トピック {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)、[extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)、[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)、[fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)、[rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)、[attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)、[id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)

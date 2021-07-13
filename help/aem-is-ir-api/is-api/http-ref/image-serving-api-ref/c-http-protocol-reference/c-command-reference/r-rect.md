---
description: 最終ビューの長方形。 最終的なビューイメージを複数のストリップまたはタイルに分解できます。これらは、別々に配信し、クライアントによってシームレスに再アセンブリでき、エッジに沿ったアーティファクトは発生しません。
solution: Experience Manager
title: rect
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 1%

---

# rect{#rect}

最終ビューの長方形。 最終的なビューイメージを複数のストリップまたはタイルに分解できます。これらは、別々に配信し、クライアントによってシームレスに再アセンブリでき、エッジに沿ったアーティファクトは発生しません。

`rect= *``*, *``*[, *`coordsizescale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード</span> </p> </td> 
  <td class="stentry"> <p>ビュー画像の左上隅からビュー長方形の左上（整数、整数）までのピクセルオフセット（<span class="varname"> scale</span>を適用した後のピクセル単位）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> サイズ</span> </p></td> 
  <td class="stentry"> <p>ROIのサイズ（ピクセル単位、整数）。 返信画像のサイズを指定します。 画像は、ビュー画像で覆われていない領域で<span class="codeph"> bgc=</span>で塗りつぶされます(リクエストに<span class="codeph"> fmt=*-alpha</span>が存在する場合は、左側が透明になります)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>スケール係数（実数） 1.0より小さい値を指定すると解像度が低下し、1.0より大きい値を指定すると解像度が高くなります。 </p></td> 
 </tr> 
</table>

このコマンドを使用すると、画像サービングはHTTP経由で大きな画像を配信できます。このコマンドを使用すると、`attribute::MaxPix`で設定されているサイズ制限を超える可能性があります。

>[!NOTE]
>
>JPEG圧縮を使用する場合に最適な結果を得るには、ストリップまたはタイルサイズをJPEGエンコーディングタイルサイズ（16 x 16ピクセル）の倍数にする必要があります。

## 例 {#section-932fcfcb41d74a29bc929e4430c49601}

印刷可能なCMYK画像を複数の最大解像度ストリップに分割して、ダウンロードファイルのサイズを小さくします。 連続した画像をリクエストする場合：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

まず、画像に関する関連情報を取得する。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

テキスト応答には、次のプロパティが含まれます。

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

この情報に基づいて、600 x 2000ピクセルのストリップを4つ選択します。 `rect=`コマンドは、ストリップのサイズと位置を記述するために使用します。

このイメージは頻繁に変更されるので、CDNまたはプロキシサーバーにキャッシュされている可能性のある古いバージョンのイメージから1つ以上のストリップが生じる可能性を最小限に抑えるために`id=`コマンドを含めます。 この目的では、`image.version`プロパティの値が使用されます。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## プロパティ {#section-aae223cee13e46d38b74680c048d945b}

属性を表示します。 現在の画層設定に関係なく適用されます。

ビュー画像の外側に広がるROIの領域は、`bgc=`で埋め込まれます。

重要な`rect=`は、`scl=`、`wid=`、`hei=`、`fit=`、`rgn=`および`align=`に合わせて&#x200B;**&#x200B;の後に適用されます。

## 初期設定 {#section-b296d3bbfb19441f87137a452b70f19a}

ビュー画像全体(`rect=0,0,width,height,1.0`)。

## 関連トピック {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) 、 [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)、 [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、 [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、 [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)、 [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)、 [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)、 [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)、 [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)

---
title: rect
description: 最終的なビューの長方形 これにより、最終的なビュー画像をいくつかのストリップまたはタイルに分解し、個別に配信し、エッジに沿ってアーティファクトを含めずにクライアントによってシームレスに再構築できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
TQID: 'https://experienceleague.adobe.com/v-sAA1KXCiZvFp6NATVZtxYxnQCji3YJZCFa-hcHQYA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 366
ht-degree: 1%

---

# rect{#rect}

最終的なビューの長方形 これにより、最終的なビュー画像をいくつかのストリップまたはタイルに分解し、個別に配信し、エッジに沿ってアーティファクトを含めずにクライアントによってシームレスに再構築できます。

`rect= *` コード `*, *` サイズ `*[, *` スケール `*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> コード </span> </p> </td> 
  <td class="stentry"> <p><span class="varname"> スケール </span>が適用された後、ビュー画像の左上隅からビュー長方形の左上隅（int、int）までのピクセルのオフセット（ピクセルで表されます）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> サイズ </span> </p></td> 
  <td class="stentry"> <p>ROIのサイズ （ピクセル単位（int、int））。 返信画像サイズを指定します。 画像は、ビューイメージでカバーされていない領域の<span class="codeph"> bgc=</span>で埋められます（または、<span class="codeph"> fmt=*-alpha</span>がリクエストに存在する場合は透明のままになります）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">尺度</span> </p></td> 
  <td class="stentry"> <p>スケール係数（実数）。 1.0より小さい値は解像度を下げ、1.0より大きい値は解像度を上げます。 </p></td> 
 </tr> 
</table>

このコマンドを使用すると、画像サービングは、HTTP経由で大きな画像を配信できます。そうしないと、`attribute::MaxPix`で設定されたサイズ制限を超えてしまいます。

>[!NOTE]
>
>最適な結果を得るには、JPEG圧縮を使用する場合、ストリップまたはタイルのサイズは、JPEG エンコーディングタイルサイズ（16 x 16 ピクセル）の倍数にする必要があります。

## 例 {#section-932fcfcb41d74a29bc929e4430c49601}

印刷可能なCMYK画像をいくつかのフル解像度ストリップに分割して、ダウンロードファイルのサイズを小さくします。 連続した画像をリクエストした場合：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

まず、画像に関する関連情報を取得します。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

テキスト応答には、次のプロパティが含まれます。

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

この情報に基づいて、4つの600 x 2000 ピクセルストリップが必要です。 `rect=` コマンドは、ストリップのサイズと位置を記述するために使用されます。

この画像は頻繁に変更されるので、`id=` コマンドが含まれます。 これにより、CDNまたはプロキシサーバーにキャッシュされている可能性のある古いバージョンの画像から1つ以上のストリップが発生する可能性を最小限に抑えることができます。 この目的では、`image.version` プロパティの値が使用されます。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## プロパティ {#section-aae223cee13e46d38b74680c048d945b}

ビュー属性。 現在のレイヤー設定に関係なく適用されます。

ビュー画像の外側に広がるROIの領域には、`bgc=`が埋め込まれています。

重要な`rect=`は、`scl=`、`wid=`、`hei=`、`fit=`、`rgn=`、および`align=`を使用して&#x200B;*after*&#x200B;に適用されます。

## 初期設定 {#section-b296d3bbfb19441f87137a452b70f19a}

変更されていないビュー画像全体（`rect=0,0,width,height,1.0`）。

## 関連トピック {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)、[extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)、[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)、[fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)、[rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)、[属性：:MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)、[id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)

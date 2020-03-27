---
description: ズームターゲットデータ なしまたはそれ以上のズームターゲットプロパティ。ズームビューアクライアントと組み合わせて使用できます。
seo-description: ズームターゲットデータ なしまたはそれ以上のズームターゲットプロパティ。ズームビューアクライアントと組み合わせて使用できます。
seo-title: ターゲット
solution: Experience Manager
title: ターゲット
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# ターゲット{#targets}

ズームターゲットデータ なしまたはそれ以上のズームターゲットプロパティ。ズームビューアクライアントと組み合わせて使用できます。

サーバーは、「 `req=targets``??`&#39; recordターミネータトークンを置き換えた後、に応答して、このフィールドのコンテンツを返します。

各ズームターゲットには、最大4つのプロパティを関連付けることができます。

` Target. *`numframe`*.frame= *``*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *`numlabel`*.label= *``*`

` Target. *`numuserData`*.userData= *``*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 番 </span> 号 </span> </p> </td> 
  <td class="stentry"> <p>ズームターゲット番号（整数）;ズームターゲットには、1から始まる順番に番号を付ける必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 枠 </span></span> </p> </td> 
  <td class="stentry"> <p>スピンセットまたはパンフレットセットの特定のフレーム/ページをターゲットにするためのオプションのフレーム/ページ番号。スピンビューアおよびパンフレットビューアの使用に指定しない場合、初期設定は0です。ズームビューアでは無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> left, top </span></span> </p> </td> 
  <td class="stentry"> <p>画像の左上からズームターゲットの長方形の左上までのピクセルオフセット（整数、整数）;は0以上に設定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 幅、高 </span> さ </span> </p> </td> 
  <td class="stentry"> <p>ズームターゲットの長方形のピクセルサイズ（整数、整数）;は0より大きい値に設定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ラベ </span> ル </span> </p> </td> 
  <td class="stentry"> <p>テキストデータ値；は、ズームターゲットリンクのテキストラベルとして使用できます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span></span> </p> </td> 
  <td class="stentry"> <p>テキストデータ値；を使用して、SKU値やホットリンクURLなど、ターゲット固有の情報をクライアントに渡すことができます。 </p> </td> 
 </tr> 
</table>

Target. *`num`*&#x200B;各ズームターゲットには.rectが必要で、画像内に完全に長方形を指定する必要があります。 その他のプロパティはすべてオプションです。

*`label`* テキスト文 *`userData`* 字列のローカリゼーションに参加します。 詳しくは、 [](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) HTTPプロトコルリファレンスの *「テキスト文字列のローカリゼーション* 」を参照してください。

スピンビューアおよびパンフレットビューアのクライアントが関与するアプリケーションの場合、ズームターゲットは、画像セットを定義するのと同じカタログレコードで定義する必要があります。 画像セットのメンバのカタログレコード内のズームターゲット定義は、ビューアでは無視されます。

Scene7ビューアは、のコマンドで既に調整済みの最大解像度画像の座標にズームターゲットが表示されることを期待しま `catalog::Modifier`す。

## プロパティ {#section-b3f8eba4985f4b00bb935d592fe770f9}

[プロパティデータ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 値です。

## 初期設定 {#section-feab29f6575e482391086a57f547543c}

なし

## 関連項目 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) 、 [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)、 [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、テキスト文字 [列のローカリゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)

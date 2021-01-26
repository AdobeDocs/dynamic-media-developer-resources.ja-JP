---
description: ズームターゲットデータ なしまたはそれ以上のズームターゲットのプロパティ。これは、ズームビューアクライアントと組み合わせて使用できます。
seo-description: ズームターゲットデータ なしまたはそれ以上のズームターゲットのプロパティ。これは、ズームビューアクライアントと組み合わせて使用できます。
seo-title: ターゲット
solution: Experience Manager
title: ターゲット
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 2%

---


# ターゲット{#targets}

ズームターゲットデータ なしまたはそれ以上のズームターゲットのプロパティ。これは、ズームビューアクライアントと組み合わせて使用できます。

&#39; `??`&#39;レコードの終端記号トークンを置き換えた後、サーバーは`req=targets`に応答してこのフィールドの内容を返します。

各ズームターゲットには、最大4つのプロパティを関連付けることができます。

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>ズームターゲット番号（整数）;ズームターゲットには、1から順に順番に番号を付ける必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame  </span> </span> </p> </td> 
  <td class="stentry"> <p>スピンセットまたはパンフレットセットの特定のフレーム/ページをターゲットにするためのオプションのフレーム/ページ番号スピンビューアおよびパンフレットビューアの使用に指定しない場合、初期設定は0です。は、ズームビューアでは無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> left, top  </span> </span> </p> </td> 
  <td class="stentry"> <p>画像の左上からズームターゲットの長方形の左上までのピクセルオフセット（整数、整数）;は0以上に設定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width, height  </span> </span> </p> </td> 
  <td class="stentry"> <p>ズームターゲットの長方形のピクセルサイズ（整数、整数）;は0より大きい値に設定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label  </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストデータ値；は、ズームターゲットリンクのテキストラベルとして使用できます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストデータ値；は、SKU値やホットリンクURLなどのターゲット固有の情報をクライアントに渡すために使用します。 </p> </td> 
 </tr> 
</table>

Target. *`num`*.rectは、各ズームターゲットに必要で、画像内に完全に長方形を指定する必要があります。その他のプロパティはすべてオプションです。

*`label`* テキスト文字列ローカライゼーション *`userData`* に参加します。詳しくは、『*HTTPプロトコルリファレンス*』の[テキスト文字列ローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)を参照してください。

スピンビューアおよびパンフレットビューアのクライアントが関与するアプリケーションの場合、ズームターゲットは、画像セットを定義しているのと同じカタログレコードで定義する必要があります。 画像セットのメンバのカタログレコードに含まれるズームターゲット定義は、ビューアでは無視されます。

Dynamic Mediaの閲覧者は、`catalog::Modifier`のコマンドで調整済みの最大解像度の画像の座標にズームターゲットが必要になります。

## プロパティ {#section-b3f8eba4985f4b00bb935d592fe770f9}

[プロパティ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) データ値。

## 初期設定 {#section-feab29f6575e482391086a57f547543c}

なし

## 関連項目 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md),  [Text Stringローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)

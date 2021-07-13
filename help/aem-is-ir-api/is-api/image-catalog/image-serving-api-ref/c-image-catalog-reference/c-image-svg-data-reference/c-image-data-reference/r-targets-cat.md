---
description: ズームターゲットデータ なしまたはそれ以上のズームターゲットプロパティ。ズームビューアクライアントと組み合わせて使用できます。
solution: Experience Manager
title: ターゲット
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 2%

---

# ターゲット{#targets}

ズームターゲットデータ なしまたはそれ以上のズームターゲットプロパティ。ズームビューアクライアントと組み合わせて使用できます。

「 `??` 」レコード終端文字トークンを置き換えた後、サーバーは`req=targets`に応答してこのフィールドの内容を返します。

各ズームターゲットには、最大4つのプロパティを関連付けることができます。

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>ズームターゲット番号（整数）ズームターゲットの番号は、1から順に連続して指定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame  </span> </span> </p> </td> 
  <td class="stentry"> <p>スピンセットまたはパンフレットセットの特定のフレーム/ページをターゲットにするオプションのフレーム/ページ番号スピンビューアおよびパンフレットビューアの使用に指定しない場合は、初期設定で0になります。はズームビューアでは無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> left, top  </span> </span> </p> </td> 
  <td class="stentry"> <p>画像の左上からズームターゲットの長方形の左上へのピクセルオフセット（整数、整数）。は0以上に設定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 幅、高さ  </span> </span> </p> </td> 
  <td class="stentry"> <p>ズームターゲットの長方形のピクセルサイズ（整数、整数）は0より大きい値にする必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label  </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストデータ値は、ズームターゲットリンクのテキストラベルとして使用できます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストデータ値を使用して、SKU値やホットリンクURLなどのターゲット固有の情報をクライアントに渡すことができます。 </p> </td> 
 </tr> 
</table>

Target. *`num`*.rectは、各ズームターゲットに対して必要で、画像内に長方形を完全に指定する必要があります。その他のプロパティはすべてオプションです。

*`label`* およびは、テ *`userData`* キスト文字列のローカライゼーションに参加します。詳しくは、「*HTTPプロトコルリファレンス*」の「[テキスト文字列のローカライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)」を参照してください。

スピンビューアクライアントとパンフレットビューアクライアントが関与するアプリケーションの場合、ズームターゲットは、画像セットを定義するのと同じカタログレコードで定義する必要があります。 画像セットのメンバのカタログレコード内のズームターゲット定義は、ビューアでは無視されます。

Dynamic Mediaのビューアは、 `catalog::Modifier`のコマンドで既に調整済みの最大解像度画像の座標でズームターゲットを表示する必要があります。

## プロパティ {#section-b3f8eba4985f4b00bb935d592fe770f9}

[プロパティ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) のデータ値。

## 初期設定 {#section-feab29f6575e482391086a57f547543c}

なし

## 関連項目 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) 、 [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)、 [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、テキスト文字列のローカ [ライゼーション](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)

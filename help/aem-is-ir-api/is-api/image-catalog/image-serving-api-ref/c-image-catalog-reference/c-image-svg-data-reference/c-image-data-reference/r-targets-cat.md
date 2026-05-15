---
description: ターゲットデータをズームします。 ズームビューア クライアントと一緒に使用できるズームターゲットプロパティは、なし以上です。
solution: Experience Manager
title: 目標
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
TQID: 'https://experienceleague.adobe.com/kP22kltIPZqErqxNKpYp2eNkII-GdYQQeiVH3wEYOvM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 1%

---

# 目標{#targets}

ターゲットデータをズームします。 ズームビューア クライアントと一緒に使用できるズームターゲットプロパティは、なし以上です。

サーバーは、&#39;`??`&#39; レコード ターミネータ トークンを置き換えた後、`req=targets`に応答してこのフィールドのコンテンツを返します。

各ズームターゲットには、最大4つのプロパティを関連付けることができます。

` Target. *`num`*.frame= *`frame`*`

` Target. *`num`*.rect= *`left,top,width,height`*`

` Target. *`num`*.label= *`label`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>ズームターゲット番号（int）。ズームターゲットには、1から始まる順に番号を付ける必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> フレーム </span> </span> </p> </td> 
  <td class="stentry"> <p>スピンまたはパンフレットセットの特定のフレーム/ページをターゲティングするためのオプションのフレーム/ページ番号。スピンおよびパンフレットビューアの使用に指定されていない場合は、デフォルトで0に設定されます。ズームビューアでは無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> 残り<span class="codeph"> <span class="varname">、上</span> </span> </p> </td> 
  <td class="stentry"> <p>画像の左上からズームターゲット長方形（int、int）の左上までのピクセルのオフセット。0以上にする必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">幅、高さ</span> </span> </p> </td> 
  <td class="stentry"> <p>ズームターゲット長方形（int、int）のピクセルサイズ。0より大きくなければなりません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ラベル </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストデータ値。ズームターゲットリンクのテキストラベルとして使用できます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ユーザーデータ </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストデータ値。SKU値やホットリンク URLなど、ターゲット固有の情報をクライアントに渡すために使用できます。 </p> </td> 
 </tr> 
</table>

ターゲット： *`num`*.rectは各ズームターゲットに必要であり、画像内で完全に長方形を指定する必要があります。 その他のプロパティはすべてオプションです。

*`label`*&#x200B;と&#x200B;*`userData`*&#x200B;はテキスト文字列のローカライズに参加しています。 詳しくは、*HTTP プロトコルリファレンス*&#x200B;の[&#x200B; テキスト文字列のローカライゼーション &#x200B;](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)を参照してください。

スピンビューアおよびパンフレットビューアのクライアントを含むアプリケーションの場合、ズームターゲットは、画像セットを定義するのと同じカタログレコードで定義する必要があります。 画像セットのメンバーのカタログレコード内のズームターゲット定義は、ビューアによって無視されます。

Dynamic Media ビューアは、`catalog::Modifier`のコマンドによって既に調整されているフル解像度の画像の座標にズームターゲットを期待しています。

## プロパティ {#section-b3f8eba4985f4b00bb935d592fe770f9}

[&#x200B; プロパティデータ &#x200B;](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md)値。

## 初期設定 {#section-feab29f6575e482391086a57f547543c}

なし

## 関連項目 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[&#x200B; カタログ：:ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256)、[&#x200B; カタログ：:Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)、[req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、[&#x200B; テキスト文字列のローカライズ &#x200B;](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)

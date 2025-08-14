---
description: ズームターゲットデータ。 なし、またはそれ以上のズームターゲットプロパティ。ズームビューアクライアントと組み合わせて使用できます。
solution: Experience Manager
title: ターゲット
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# ターゲット{#targets}

ズームターゲットデータ。 なし、またはそれ以上のズームターゲットプロパティ。ズームビューアクライアントと組み合わせて使用できます。

サーバーは、「`req=targets`」レコードのターミネータトークンを置き換えた後、`??` に応答してこのフィールドの内容を返します。

各ズームターゲットには、最大 4 つのプロパティを関連付けることができます。

` Target. *`num`*.frame= *`frame`*`

` Target. *`num`*.rect= *`left,top,width,height`*`

` Target. *`num`*.label= *`label`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>ズームターゲットの番号（整数）。ズームターゲットには、1 から始まる番号を連続して付ける必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> フレーム </span> </span> </p> </td> 
  <td class="stentry"> <p>スピンまたはパンフレットのセットの特定のフレーム/ページをターゲットにするためのオプションのフレーム/ページ番号。スピンビューアおよびパンフレットのビューアで使用するために指定しない場合は、デフォルトで 0 になります。ズームビューアでは無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> left, top </span> </span> </p> </td> 
  <td class="stentry"> <p>画像の左上からズームターゲットの長方形の左上へのピクセルオフセット（int、int）。0 以上である必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> 幅 <span class="codeph"> 高さ <span class="varname"></span> の </span> </p> </td> 
  <td class="stentry"> <p>ズームターゲット長方形のピクセルサイズ （int、int）。0 より大きい値を指定する必要があります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストデータ値。ズームターゲットリンクのテキストラベルとして使用できます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>テキストデータ値。SKU 値やホットリンク URL など、ターゲット固有の情報をクライアントに渡すために使用できます。 </p> </td> 
 </tr> 
</table>

ターゲット。 *`num`*.rect は各ズームターゲットに必要で、画像内で長方形を完全に指定する必要があります。 その他のプロパティはすべてオプションです。

テキスト文字列のローカライゼーションには *`label`* と *`userData`* が使用されます。 詳しくは、[HTTP プロトコルリファレンス ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) の *テキスト文字列のローカリゼーション* を参照してください。

スピンおよびパンフレットのビューアクライアントに関係するアプリケーションの場合、画像セットを定義したのと同じカタログレコードでズームターゲットを定義する必要があります。 画像セットのメンバーのカタログレコード内のズームターゲット定義は、ビューアでは無視されます。

Dynamic Media ビューアでは、`catalog::Modifier` のコマンドで既に調整されたフル解像度画像の座標にズームターゲットが必要です。

## プロパティ {#section-b3f8eba4985f4b00bb935d592fe770f9}

[ プロパティデータ ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 値。

## 初期設定 {#section-feab29f6575e482391086a57f547543c}

なし

## 関連項目 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256)、[catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)、[req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、[ テキスト文字列のローカライズ ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)

---
description: 画像/メタデータのバージョン 頻繁に変更されるコンテンツを扱う場合、Akamai、ブラウザーキャッシュ、会社のプロキシサーバーキャッシュなどのキャッシュネットワーク内のサーバーには、古い画像サービング応答が格納される場合があります。
seo-description: 画像/メタデータのバージョン 頻繁に変更されるコンテンツを扱う場合、Akamai、ブラウザーキャッシュ、会社のプロキシサーバーキャッシュなどのキャッシュネットワーク内のサーバーには、古い画像サービング応答が格納される場合があります。
seo-title: id
solution: Experience Manager
title: id
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 3%

---


# id{#id}

画像/メタデータのバージョン 頻繁に変更されるコンテンツを扱う場合、Akamai、ブラウザーキャッシュ、会社のプロキシサーバーキャッシュなどのキャッシュネットワーク内のサーバーには、古い画像サービング応答が格納される場合があります。

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>バージョン文字列。 </p> </td> 
 </tr> 
</table>

画像サービングには、古いキャッシュエントリがアプリケーションで使用される可能性を低減するためのバージョン管理メカニズムが含まれています。 このメカニズムでは、`req=props`を使用して、画像データとメタデータ(画像マップやズームターゲットデータなど)のバージョン識別子文字列を取得します。 次に、`id=`コマンドを使用して、バージョン識別子文字列をキャッシュ可能な画像サービング要求に追加します。

ソース画像またはメタデータが変更されると、対応するバージョンIDの値も変更されます。 `id=`コマンドに最新のバージョンid値を含めると、古いキャッシュエントリにアクセスできなくなります。

次の表に、各`req=`型に使用するバージョン識別子文字列をリストします。

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req=type</b> </th> 
   <th class="entry"> <b> req=propsのバージョン識別子</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> マップ </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> mask </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> ターゲット </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> userdata </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` 上記に記載されていない型は、短いTTL ( `attribute::NonImgExpiration`)を持つか、応答がまったくキャッシュできません。そんな依頼を受け入れるの `id=` は利点がない。

## プロパティ {#section-62e973d0d5884abebbb0679f9278ae2c}

要求属性。 （オプション）常にサーバーから無視されます。

## 初期設定 {#section-96136720c82842c89505347ec39e6024}

なし

## 例 {#section-a5fb871e0ec8485c91c4fca78895d17f}

使用例については、[rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)の説明を参照してください。

## 関連トピック {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3),  [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a),  [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)

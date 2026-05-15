---
title: id
description: 画像/メタデータバージョン： 頻繁に変更されるコンテンツを扱う場合、Akamai、ブラウザーキャッシュ、企業プロキシサーバーキャッシュなどのキャッシュネットワーク内のサーバーは、画像サービング応答を保存する場合があります。この応答は長期間にわたって古くなる可能性があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
TQID: 'https://experienceleague.adobe.com/TPRGzHQ-TxTusgeqo2eLlCG0fNOtmJ1IHIxuUy8bh2I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 3%

---

# id{#id}

画像/メタデータバージョン： 頻繁に変更されるコンテンツを扱う場合、Akamai、ブラウザーキャッシュ、企業プロキシサーバーキャッシュなどのキャッシュネットワーク内のサーバーは、画像サービング応答を保存する場合があります。この応答は長期間にわたって古くなる可能性があります。

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>バージョン文字列。 </p> </td> 
 </tr> 
</table>

画像サービングには、古いキャッシュエントリがアプリケーションで使用される可能性を減らすのに役立つバージョン管理メカニズムが含まれています。 このメカニズムでは、`req=props`を使用して、画像データとメタデータ（画像マップやズームターゲットデータなど）のバージョン識別子文字列を取得します。 次に、`id=` コマンドを使用してキャッシュ可能な画像サービング要求にバージョン識別子の文字列を追加します。

ソース画像またはメタデータが変更されると、対応するバージョン ID値も変更されます。 `id=` コマンドに最新のバージョン ID値を含めると、古いキャッシュ エントリにアクセスできなくなります。

次の表に、各`req=` タイプに使用されるバージョン識別子の文字列を示します。

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> req=props</b>の<b> バージョン識別子 </th> 
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
   <td> <p> マスク </p> </td> 
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

上記に記載されていない`req=`型は、短いTTL （`attribute::NonImgExpiration`）を持っているか、その応答をまったくキャッシュできません。そのような要求に`id=`を含めることは利点がありません。

## プロパティ {#section-62e973d0d5884abebbb0679f9278ae2c}

リクエスト属性： オプション。 常にサーバーから無視されます。

## 初期設定 {#section-96136720c82842c89505347ec39e6024}

なし

## 例 {#section-a5fb871e0ec8485c91c4fca78895d17f}

使用例については、[rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)の説明を参照してください。

## 関連トピック {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)、[rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)、[ カタログ：:Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)、[属性：:NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)

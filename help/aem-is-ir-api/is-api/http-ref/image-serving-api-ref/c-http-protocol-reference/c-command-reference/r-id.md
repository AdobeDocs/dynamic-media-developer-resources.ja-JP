---
title: id
description: 画像/メタデータのバージョン。 頻繁に変化するコンテンツを操作する場合、Akamai、ブラウザーキャッシュ、会社のプロキシサーバーキャッシュなどのキャッシュネットワーク内のサーバーには、画像サービング応答が格納されますが、この応答は一定期間古くなっている可能性があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 3%

---

# id{#id}

画像/メタデータのバージョン。 頻繁に変化するコンテンツを操作する場合、Akamai、ブラウザーキャッシュ、会社のプロキシサーバーキャッシュなどのキャッシュネットワーク内のサーバーには、画像サービング応答が格納されますが、この応答は一定期間古くなっている可能性があります。

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>バージョン文字列。 </p> </td> 
 </tr> 
</table>

画像サービングにはバージョン管理メカニズムが含まれており、アプリケーションで古いキャッシュエントリが使用される可能性を減らすことができます。 このメカニズムは、 `req=props` 画像データおよびメタデータ（画像マップやズームターゲットデータなど）のバージョン識別子文字列を取得する。 次に、バージョン識別子文字列が、 `id=` コマンドを使用します。

ソース画像またはメタデータが変更されると、対応するバージョン ID の値も変更されます。 最新のバージョン ID 値を `id=` コマンドを使用すると、古いキャッシュエントリにアクセスできなくなります。

次の表に、それぞれに使用するバージョン識別子文字列を示します `req=` 型：

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req=type</b> </th> 
   <th class="entry"> <b> req=props のバージョン識別子</b> </th> 
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

`req=` 上記のリストにないタイプは、短い TTL ( `attribute::NonImgExpiration`) またはその応答は、まったくキャッシュできません。 `id=` を設定します。

## プロパティ {#section-62e973d0d5884abebbb0679f9278ae2c}

要求属性。 オプション。サーバーでは常に無視されます。

## 初期設定 {#section-96136720c82842c89505347ec39e6024}

なし

## 例 {#section-a5fb871e0ec8485c91c4fca78895d17f}

詳しくは、 [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) 例：使用方法。

## 関連トピック {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
